% 6G5Z3001_1314 \\\\ Mathematical Methods
% Killian O'Brien
% Oct 2013
# Multi-variable calculus

## Multi-variable calculus \\\\ Higher-order derivatives (sec. 1.4)

For a function, $f$ of two variables, $x$ and $y$, the second-order derivatives are denoted by 
$$\begin{align} 
\frac{ \partial^2 f }{\partial x^2} &= \frac{\partial}{\partial x} \left ( \frac{\partial f}{\partial x} \right ) , \\
\frac{ \partial^2 f }{\partial y^2} &= \frac{\partial}{\partial y} \left ( \frac{\partial f}{\partial y} \right ), \\
\frac{ \partial^2 f }{\partial x \partial y} &= \frac{\partial}{\partial x} \left ( \frac{\partial f}{\partial y}\right ) , \\
\frac{ \partial^2 f }{\partial y \partial x} &= \frac{\partial}{\partial y} \left ( \frac{\partial f}{\partial x}\right ) .
\end{align}$$
Some of the third-order partial derivatives would be
$$\begin{align}
\frac{ \partial^3 f }{\partial x^3} &= \frac{\partial}{\partial x} \left (\frac{ \partial^2 f }{\partial x^2} \right ) , \\
\frac{ \partial^3 f }{\partial x \partial y^2} &= \frac{\partial}{\partial x} \left (\frac{ \partial^2 f }{\partial y^2} \right ).
\end{align}$$

Notice how each higher-order partial derivative symbol is read and interpreted as a composition of differentiation operators. 

### Example 1.3

Use the function 
$$
f(x,y) = x^2 y^3 \tan{(2x)} ,
$$
from the previous example and find all four of its second derivative.

Check our answers with a Sage cell.
<div class="compute"><script type="text/x-sage">
var('x,y')
f(x,y) = x^2 * y^3 * tan(2*x)
diff(f,x,x)
</script></div>

## Multi-variable calculus \\\\ Clairaut's Theorem & functions of more than two variables

Note that $\frac{ \partial^2 f }{\partial x \partial y} $ = $\frac{ \partial^2 f }{\partial y \partial x}$. This is true in general for functions whose derivatives exist and are continuous.

### Theorem 1.1 (Clairaut)
Let $f: \mathbb{R}^2 \to \mathbb{R}$. Suppose that all the second-order partial derivatives of $f$ exist and are continuous. Then 
$$
\frac{ \partial^2 f }{\partial x \partial y} = \frac{ \partial^2 f }{\partial y \partial x}.
$$

### Functions of more than two variables (sec. 1.5)

The principle we outlined earlier for differentiating functions of two variables readily extends to functions of three or more variables. 

### Example 1.4
Find the three first-order partial derivatives of the function $g$ defined by 
$$
g(x,y,x) = x^2 y^4 z^3 .
$$

<div class="compute"><script type="text/x-sage">
var('x,y,z')
g(x,y,z) = x^2 * y^4 * z^3
show(diff(g,z))
</script></div>

## Multi-variable calculus \\\\ Tangent planes

### Tangent plane to a surface (sec. 1.6)

Let $(x,y,z)$ be the usual Cartesian coordinate system for $\mathbb{R}^3$ and let $S$ be the surface in $\mathbb{R}^3$ defined by an equation 
$$
z = f(x,y).
$$
Let $P$ be a point on $S$ with coordinates $(x_P, y_P, z_P)$. The tangent plane $T$ in $\mathbb{R}^3$ will have  an equation of the form 
$$
z = \alpha x + \beta y + \gamma \label{E:plane}, 
$$
where $\alpha$ and $\beta$ are the gradients of $T$ in the $x$ and $y$ directions. But since $T$ is a tangent plane these gradients are the same as those of $S$ in the $x$ and $y$ directions. Therefore

$$\begin{align}
\alpha &= \frac{\partial z}{\partial x} = \left. \frac{\partial f}{\partial x} \right |_{(x,y)=(x_P, y_P)}, \\
\beta &= \frac{\partial z}{\partial y} = \left. \frac{\partial f}{\partial y} \right |_{(x,y)=(x_P, y_P)} 
\end{align}$$

Since the point $P$ is on $T$ and $S$ we have 
$$\begin{align}
& z_p = \alpha  x_P + \beta y_P + \gamma = f(x_P, y_P), \\
\Rightarrow & \gamma = f(x_P, y_P) - \alpha x_P - \beta y_P. \label{E:planegamma}
\end{align}$$
These results show how the equation of a tangent plane, can be determined from the function, $f$, defining the surface and the base point $(x_P, y_P)$. 

### Example 1.5

Determine the tangent plane to the surface defined by
$$
z = x^2 y + 2y^2 + x + 1 ,
$$
at the point $(x,y)=(2,3)$.

<div class="compute"><script type="text/x-sage">
f(x,y)=x^2 * y + 2*y^2 + x + 1 ;
p=plot3d(f(x,y), (x, -10, 14), (y, -10, 16), opacity=0.8)
q=plot3d(12 * x + 16 * y - 37, (x, -10, 14), (y, -10, 16), color='red', opacity=0.8)

show(p+q)
</script></div>

![Tangent Plane plot](https://www.dropbox.com/s/ni1plhc3udyyxcj/tangent-plane.png)
















 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 <!--- 
 <div class="compute"><script type="text/x-sage"><div class="compute"><script type="text/x-sage">
@interact
def tline(ep=slider(0.0001,4,0.1,0)):
          p=plot(sin(x), (x, 0, 2*pi));
          a=pi/2;
          u=a+ep;
          slope=(sin(u)-sin(a))/(u-a);
          q=plot(slope*(x-pi/2)+sin(pi/2), (x,0,2*pi), color='red');
          (p+q).show();
</script></div> </script></div> 


[`cloud.sagemath.com`](https://cloud.sagemath.com).
 --->
