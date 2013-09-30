% 6G5Z3001_1314 \\\\ Mathematical Methods
% Killian O'Brien
% Sep 2013
# Introduction

## Teaching & Assessment
* Lectures (3 per week)		
	Stephen, Killian and Stephen/Killian.	
	3rd lecture alternates between S & K and will often serve as a large examples class.
* Tutorials (1 per week)		
	Stephen, Killian or Andy		
	Your Maths Methods tutor is also you Personal & Academic Tutor
* Unit Content		
	Stephen -- Linear Algebra	
	Killian -- Analytical Methods: Multi-variable calculus; Laplace transforms; Fourier series.
* Assessment	
	* Coursework (40%)
	* Exam (60%)
* Lots of information on Moodle	
	* [Mathematical Methods Unit Moodle Area](http://moodle.mmu.ac.uk/course/view.php?id=35024)
	* [Mathematics Undergraduate Network Moodle Area](http://moodle.mmu.ac.uk/course/view.php?id=30790)


## Analytical Methods \\\\ introduction
We will cover three main areas

* Multi-variable calculus			
	*The differentiation and integration of functions of more than one variable.*
* Laplace Transforms		
	*A method for solving certain differential equations using a transform of the unknown function.*
* Fourier Series and Transform		
	*A method to decompose a wide class of functions into an infinite series of standard periodic functions (sines and cosines).*

## Multi-variable calculus \\\\ the partial derivative

### Definition of derivative of a function of a single variable (sec. 1.1)

Recall that for a function, $f: \mathbb{R} \to \mathbb{R}$, of a single variable the derivative, $f'(a)$, of $f$ at a point $a$ is defined by 
$$f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x-a}.$$

An equivalent formulation of the definition, using alterntaive notation, is 
$$
\frac{df}{dx} = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}.
$$ 

## Multi-variable calculus \\\\ the partial derivative
### Defintion of partial derivative (for function of two-variables) (sec. 1.2)

Let $f$ be a function of the two independent variables $x$ and $y$. The *partial derivative*, $\frac{ \partial f}{\partial x}$,  of $f$ *with respect to* $x$ is defined as 
$$
\frac{\partial f}{\partial x} = \lim_{\delta x \to 0} \frac{f(x + \delta x, y) - f(x,y)}{\delta x}.
$$

Similarly we can define the partial derivative of $f$ with respect to the other variable.
The *partial derivative*, $\frac{ \partial f}{\partial y}$,  of $f$ *with respect to* $y$ is defined as 
$$
\frac{\partial f}{\partial y} = \lim_{\delta y \to 0} \frac{f(x , y+ \delta y) - f(x,y)}{\delta y}.
$$

## Multi-variable calculus \\\\ the partial derivative
### Example 1.1 (sec. 1.2)

Consider the function $f$ defined by 
$$f(x,y) = x^2 y.$$
The partial derivatives are evaluated as follows,
$$\begin{align}
\frac{\partial f}{\partial x} 
&= \lim_{\delta x \to 0} \frac{f(x + \delta x, y) - f(x,y)}{\delta x} ,\\
&= \lim_{\delta x \to 0} \frac{\left ( x + \delta x \right )^2 y - x^2 y}{\delta x} ,\\
&= \lim_{\delta x \to 0} \frac{2x \delta x + (\delta x)^2}{\delta x} y ,\\
&= \lim_{\delta x \to 0} ( 2x + \delta x ) y ,\\
&= 2xy.
\end{align}
$$
A similar calculation will show that 
$$ \frac{ \partial f}{\partial y} = x^2. $$

## Multi-variable calculus \\\\ the partial derivative

In practice we make use of all the standard derivatives and properties of differentiation that we have from the one-variable case, along with the following principle:

>when differentiating a multi-variable function, $f$ say, with respect to the variable $x$, we treat the other variables as if they were constants, so that $f$ becomes a function of the single-variable $x$, and then differentiate $f$ using the standard one-variable differentiation techniques

### Example 1.2 

Consider the function $f$ defined by 
$$ f(x,y) = x^2 y^3 \tan{(2x)} ,$$
and find its partial derivative $\frac{\partial f}{\partial x}$ and $\frac{\partial f}{\partial y}$.

### Checking your work

* Verify your work with others
* Use Matlab

~~~
>> syms x y
>> diff(x^2*y^3*tan(2*x),x)

ans =
 
x^2*y^3*(2*tan(2*x)^2 + 2) + 2*x*y^3*tan(2*x)
~~~

* Use a [Sage cell](http://sagecell.sagemath.org)

<div class="compute"><script type="text/x-sage">
var('x,y');
f(x,y)=x^2 * y^3 * tan(2*x);
show(diff(f,x))
</script></div>

## Multi-variable calculus \\\\ the partial derivative

### Alternative notation (pg. 2,3)

The derivatives $\frac{\partial f}{\partial x}$ and $\frac{\partial f}{\partial y}$ can also be written $f_x$ and $f_y$ respectively. Makes it easier to refer to values of the drivative, e.g. 
$$ f_x (0.1,4.5) \text{ as opposed to } \left. \frac{\partial f}{\partial x} \right |_{(x,y)=(0.1,4.5)} .$$

However the delta notation lends itself to seeing differentiation as an *operator* applied to a function, i.e.
$$ \frac{\partial }{\partial x} \left ( \cos(xy) \right ) = -y\sin(xy).$$

## Multi-variable calculus \\\\ the partial derivative

### Graphical interpretation

Let $(x,y,z)$ be the usual Cartesian coordinate system for $\mathbb{R}^3$. The equation 
\beq 
z = f(x,y),
\eeq
defines a surface in $\mathbb{R}^3$. For each pair $(a,b)$, the value of $z=f(a,b)$ gives the height of the surface above or below (accordingly as $z$ is positive or negative) the $(x,y)$-plane. An example is shown in figure 1.1 (pg. 3)
When evaluated at the point $(a,b)$, the partial derivatives,
$$
\left. \frac{\partial f}{\partial x} \right |_{(x,y)=(a,b)}, \text{ and } 
\left. \frac{\partial f}{\partial y} \right |_{(x,y)=(a,b)},
$$
give the gradient of the surface at the point $(a,b)$ in the $x$ and $y$ directions respectively. 

## Multi-variable calculus \\\\ the partial derivative

### Recommended reading and suggested activities

* Revise ordinary (one variable) derivatives: derivatives of standard functions, properties of the derivative (linearity, product rule, quotient rule, chain rule, ... )

* [*Schaum's Outlines of Calculus*](http://prism.talis.com/mmu/items/1954431) by Ayres & Mendelson: Chapter 48 Partial Derivatives

* Notes: Read section 1.4 and begin Exercise 1.1 Qs. 1,2,3

* Explore Matlab commands: `diff`, `ezsurf`, `ezplot3`, ...

Learning about the Sage software is not a requirement of the course. I will use it mainly for showing examples in lectures and verifying calculations. However if you are interested in mathematics on the computer and in programming then you should definately explore it.

* Explore Sage, [`www.sagemath.org`](http://www.sagemath.org) and [`cloud.sagemath.org`](http://cloud.sagemath.org)




 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
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
