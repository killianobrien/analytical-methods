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
>when differentiating a multi-variable function, $f$ say, with respect to the variable $x$, we treat the other variables as if they were constants, so that $f$ becomes a function of the single-variable $x$, and then differentiate $f$ using the standard one-variable differentiation techniques
 
 
 
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
 --->
