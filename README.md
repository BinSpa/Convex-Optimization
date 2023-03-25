# <center>home work 1

$${Coursework (1) \ for \ {Introductory\ Lectures\ on \ Optimization}}$$
$${GuoYulong} \\ {22221271}\\
{March. 28, 2023}$$



Excercise 1:
    
Prove that the following univariate functions are in the set of $\mathcal{F}^1(\mathbb{R})$
	\begin{align}
	f(x) &= e^x,\nonumber \\
	f(x) &= |x|^p,\; p > 1,\nonumber \\
	f(x) &= \frac{x^2}{1 + |x|},\nonumber \\
	f(x) &= |x| - \ln (1 + |x|).\nonumber
	\end{align}
Check the above functions are strongly convex or not. If yes, calculate the convexity parameter $\mu$.


Proof 1:
    
Definition of the Convex Function:
    A continuously differentiable function $f(\cdot)$ is called convex on a convex set $\mathcal{Q}$, $f \in \mathcal{F}^1(\mathcal{Q}^n)$ if for any $x,y \in \mathcal{Q}$ we have
$$f(y) \geq f(x)+<\nabla{f(x)}, y-x>$$
if $-f(x)$ is convex, we call $f(x)$ concave.

1. the function $f(x) = e^x$ is in the set of $\mathcal{F}^1(\mathbb{R})$

    Proof:
    
    we can assume that $y \geq x$, then we have:
    $$e^y-e^x=e^{\zeta}(y-x)$$
    where $x \leq \zeta \leq y$, thus $e^{\zeta} \geq e^x$, the we have:
    \begin{align}
    e^y-e^x &\geq e^x(y-x)\\
    f(y)-f(x)&\geq \nabla f(x)+<f(x),y-x>
    \end{align}
2. the function $f(x) = |x|^p,\; p > 1$ is in the set of $\mathcal{F}^1(\mathbb{R})$
    
    Proof:
    
    $$\lim_{x \to 0^-} \frac{f(x)-f(0)}{x-0}=\lim_{x \to 0^+} \frac{f(x)-f(0)}{x-0}=0$$
    thus, $f(x)$ is differentiable on $\mathbb{R}$
    
    if $p$ is even:
    $$\nabla f(x)=px^{p-1}$$
    if $p$ is odd:
    $$\nabla f(x)=\begin{cases} px^{p-1}，x\geq 0 \\ -px^{p-1}， x<0 \end{cases}$$
                                                             the $f(x)$ is Monotonically increasing on $\mathbb{R}$.
if $x\leq y$, we have:                                                                   $$\begin{align}
      f(y)-f(x) &= \nabla f(\zeta)(y-x),  x\leq\zeta\leq y\\                      &\geq \nabla f(x)(y-x) \\
                                                                   f(y)&\geq f(x)+<f(x), y-x> \end{align}$$         then we get the result.
    
3. the function $f(x) = \frac{x^2}{1 + |x|}$ is in the set of $\mathcal{F}^1(\mathbb{R})$
    
    Proof:
    $$f(x)=\begin{cases} \frac{x^2}{1+x}, x\geq 0 \\ \frac{x^2}{1-x}, x<0 \end{cases}$$                                                        
$$\lim_{x \to 0^-}\frac{f(x)-f(0)}{x-0}=\lim_{x \to 0^+}\frac{f(x)-f(0)}{x-0}=0$$
    thus, f(x) is differentiable on $\mathbb{R}$.           then we can get the $\nabla f(x)$:                   $$\nabla f(x)=\begin{cases} 1-\frac{1}{(1+x)^2},\, x\geq 0 \\ \frac{1}{(1-x)^2}-1,\, x<0 \end{cases} $$
    then we have:
$$\nabla^2 f(x)=\begin{cases} \frac{2}{(1+x)^3},\, x\geq 0\\ \frac{2}{(1-x)^3},\, x<0 \end{cases}$$
    we can get that the $\nabla^2f(x) > 0$, so the $\nabla f(x)$ is Monotonically increasing on $\mathbb{R}$.
    we can assume that $x\leq y$:
$$\begin{align}f(y)-f(x)&=\nabla f(\zeta)(y-x),x\leq\zeta\leq y\\ &\geq\nabla f(x)(y-x)\\ f(y)&\geq f(x)+<f(x),y-x>\end{align}$$
    The same is true for x>y.
    
4. the function $f(x) = |x| - \ln (1 + |x|)$ is in the set of $\mathcal{F}^1(\mathbb{R})$
    
    Proof:
    $$\lim_{x \to 0^-}\frac{f(x)-f(0)}{x-0}=\lim_{x \to 0^+}\frac{f(x)-f(0)}{x-0}=0$$
    thus $f(x)$ is differentiable on $\mathbb{R}$.
    
    then we can get $\nabla f(x)$:
    $$\nabla f(x)=\begin{cases}\frac{x}{1+x},\, x\geq 0 \\ \frac{x}{1-x},\, x<0 \end{cases}$$
                          
    we can get that $\nabla f(x)\geq0$
$$\nabla^2f(x)=\begin{cases}\frac{1}{(1+x)^2},\, x\geq 0 \\ \frac{1}{(1-x)^2},\, x<0 \end{cases}$$

    we can get that $\nabla^2f(x)\geq 0$, $\nabla f(x)$ is Monotonically increasing, we have:

    if $x\leq y$ :
$$\begin{align}f(y)-f(x)&=\nabla f(\zeta)(y-x),\,x\leq\zeta\leq y\\ 
&\geq \nabla f(x)(y-x)\\
f(y)&\geq f(x)+<f(x),y-x>\end{align}$$
the same is true when $x>y$.

Proof2:

Definition of the strong convex function:
A continuous differentiable function $f(\cdot)$ is called strong convex on $\mathbb{R}$, named $f \in \mathcal{F}^1_\mu(Q, ||\cdot||)$ , if there is a constant $\mu > 0$, make it to any $x,y\in \mathcal{Q}$, we have: $$f(y)\geq f(x)+<\nabla f(x), y-x>+\frac{1}{2}\mu||y-x||^2$$
the constant $\mu$ is called the convex parameter of function $f$.

Theorem:
Assume that function $f$ is quadratic continuous differentiable on set $\mathcal{Q}$ , $f\in \mathcal{F}^2_{\mu}(\mathcal{Q}, ||\cdot||)$ if and only if for any $x\in \mathcal{Q}$ and $h\in \mathbb{R}$, we have:$$<\nabla^2f(x)h, h>\,\geq \,\mu||h||^2$$
In the case of standard Euclidean norms, the conditon can be written as$$\nabla^2f(x)\,\succeq\,\mu I_n,\quad x\in \mathcal{Q}$$

1. the function $f(x) = e^x$ is not a strong convex function.
    $$\nabla^2f(x)=e^x$$
for any $\mu>0$, $e^x-\mu<0$ is established when $x<ln\mu$, thus $f(x)=e^x$ is not strong convex.

2. the function $f(x) = |x|^p,\; p > 1$ is not a strong convex function.

    if $p$ is even:
    $$\nabla^2f(x)=p(p-1)x^{p-2}$$
    if $p$ is odd:
    $$\nabla^2 f(x)=\begin{cases} p(p-1)x^{p-2}，x\geq 0 \\ -p(p-1)x^{p-2}， x<0 \end{cases}$$
the minimum of the $\nabla^2f(x)$ is $0$. Thus, the function is not strong convex.
                                
3. the function $f(x) = \frac{x^2}{1 + |x|}$ is not a strong convex function.
    $$\nabla^2 f(x)=\begin{cases} \frac{2}{(1+x)^3},\, x\geq 0\\ \frac{2}{(1-x)^3},\, x<0 \end{cases}$$
for $\lim_{x\to +\infty}\nabla^2f(x)=\lim_{x\to -\infty}\nabla^2f(x)=0$, thus, there is no $\mu>0$ satisfy the definition.
4. the function $f(x) = |x| - \ln (1 + |x|)$ is not a strong convex function.
    $$\nabla^2f(x)=\begin{cases}\frac{1}{(1+x)^2},\, x\geq 0 \\ \frac{1}{(1-x)^2},\, x<0 \end{cases}$$
for $\lim_{x\to +\infty}\nabla^2f(x)=\lim_{x\to -\infty}\nabla^2f(x)=0$, thus, there is no $\mu>0$ satisfy the definition.
\begin{excercise}\label{e2}
	\begin{definition}
		A mapping $\Phi:\mathbb{H}\to\mathbb{R}_+$ is said to be a norm on $\mathbb{H}$ if it satisfies the following axioms:
		\begin{itemize}
			\item definiteness: $\forall x\in\mathbb{H},\Phi(x)=0\Leftrightarrow x=0;$
			\item homogeneity: $\forall x\in\mathbb{H},\forall \alpha \in\mathbb{R},\Phi(\alpha x)=|\alpha|\Phi(x);$
			\item triangle inequality: $\forall x,y\in\mathbb{H},\Phi(x+y)\leq\Phi(x)+\Phi(y).$
		\end{itemize}
	\end{definition}
	Suppose a vector norm $\left\lVert \cdot\right\rVert _p$ on $ \mathbb{R}^m$ and a vector norm $\left\lVert \cdot\right\rVert _q$ on $ \mathbb{R}^n$ are given, 
	show that the induced norm: $\left\lVert A\right\rVert _{p,q}=\sup_{x\neq0}\frac{\left\lVert Ax\right\rVert _p}{\left\lVert x\right\rVert _q}$ is a norm, where $A \in \mathbb{R}^{m\times n}$, $x\in\mathbb{R}^n$ with $x\neq0$.
\end{excercise}

\begin{PROOF}{e2}
	bla.bla... bla bla.. bla.
\end{PROOF}


Excercise 3

Calculate the gradient and Hessian of the following multivariate functions and then prove that under which condition they are (strongly) convex.  
	\begin{align}
	f(x) &= \left\lVert Ax-b\right\rVert _2^2,where\quad A\in\mathbb{R}^{n\times d},x\in\mathbb{R}^{d},b\in\mathbb{R}^n, \nonumber \\
	f(w) &= \frac{1}{m}\sum_{i=1}^m\log(1+\exp(-y_i\langle w,x_i\rangle)),where\quad y_i\in\{-1,1\},x_i\in\mathbb{R}^n,w\in\mathbb{R}^n.\nonumber
	\end{align}

Proof:
    
1. 
$$f(x)=\sum_{i=1}^{n}(\sum_{j=1}^{d}a_{ij}x_i-b_i)^2$$ 
$$\frac{\partial f}{\partial x_i} = \sum_{i=1}^{n}2a_{ij}\sum_{j=1}^{d}a_{ij}x_i-b_i$$ $$\nabla f(x) = 2A^{T}(Ax-b)$$ 
$$\nabla^2 f(x) = 2A^TA$$
    
if there is a $\mu>0$ make $\nabla^2f(x)\succeq \mu I_d$, then $f(x)$ is strong convex.

2. 
$$\frac{\partial f(\omega)}{\partial \omega_k}=\frac{1}{m}\sum_{i=1}^{m}\frac{-y_ix_{ik}}{1+exp(-y_i\langle \omega,\,x_i\rangle)}$$
$$\nabla f(\omega)=
\begin{bmatrix}
{\frac{1}{m}\sum_{i=1}^{m}\frac{-y_ix_{i0}}{1+exp(-y_i\langle \omega,\,x_i\rangle)}}\\
{\vdots}\\
{\frac{1}{m}\sum_{i=1}^{m}\frac{-y_ix_{in}}{1+exp(-y_i\langle \omega,\,x_i\rangle)}}
\end{bmatrix}$$
$$\nabla^2f(\omega)=\begin{bmatrix}
{\frac{1}{m}\sum_{i=1}^{m}\frac{exp(-y_i\langle \omega,\,x_i\rangle)\cdot y_i^2\cdot x_{i0}^2}{(1+exp(-y_i\langle \omega,\,x_i\rangle))^2}}&{\cdots}&{\frac{1}{m}\sum_{i=1}^{m}\frac{exp(-y_i\langle \omega,\,x_i\rangle)\cdot y_i^2\cdot x_{i0}x_{in}}{(1+exp(-y_i\langle \omega,\,x_i\rangle))^2}}\\
{\vdots}&{\ddots}&{\vdots}\\
{\frac{1}{m}\sum_{i=1}^{m}\frac{exp(-y_i\langle \omega,\,x_i\rangle)\cdot y_i^2\cdot x_{in}x_{i0}}{(1+exp(-y_i\langle \omega,\,x_i\rangle))^2}}&{\cdots}&{\frac{1}{m}\sum_{i=1}^{m}\frac{exp(-y_i\langle \omega,\,x_i\rangle)\cdot y_i^2\cdot x_{in}^2}{(1+exp(-y_i\langle \omega,\,x_i\rangle))^2}}
\end{bmatrix}$$


\begin{excercise}\label{e4}
Given a function $f(x)\in \mathcal{F} ^{1,1}_l(\mathbb{R}^n)$.
\begin{enumerate}
	\item Prove that the function $g(t)=f(x+ty)$ is convex;
	\item Calculate $\lim_{t\to 0^+}\frac{g(t)-g(0)}{t}$;
	\item Suppose that g is convex and not necessarily smooth, show that there exists a constant h, such that $g(t)\geq g(0)+\langle h,t\rangle$;
	\item Show that there exists a function h(x), such that $f(y)\geq f(x)+\langle h(x),y-x\rangle$.
\end{enumerate}
\end{excercise}

\begin{PROOF}{e4}
bla.bla... bla bla.. bla.
\end{PROOF}



\end{document}