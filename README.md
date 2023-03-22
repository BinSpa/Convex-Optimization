# <center>home work 1

$${Coursework (1) \ for \ {Introductory\ Lectures\ on \ Optimization}}$$
$${GuoYulong} \\ {22221271}\\
{March. 28, 2023}$$



Excercise 1:Prove that the following univariate functions are in the set of $\mathcal{F}^1(\mathbb{R})$
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
    e^y-e^x &\geq e^x(y-x)
    f(y)-f(x)&\geq 
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

if $x\geq 0, \, y\geq 0, x\leq y$, we have:                                                                   $$\begin{align}
      f(y)-f(x) &= \nabla f(\zeta)(y-x),  x\leq\zeta\leq y\\                      &\geq \nabla f(x)(y-x) \\
                                                                   f(y)&\geq f(x)+<f(x), y-x> \end{align}$$         then we get the result.
    
3. the function $f(x) = \frac{x^2}{1 + |x|}$ is in the set of $\mathcal{F}^1(\mathbb{R})$
    
    Proof:
    $$$$
4. the function $f(x) = e^x$ is in the set of $\mathcal{F}^1(\mathbb{R})$

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


\begin{excercise}\label{e3}
	Calculate the gradient and Hessian of the following multivariate functions and then prove that under which condition they are (strongly) convex  
	\begin{align}
	f(x) &= \left\lVert Ax-b\right\rVert _2^2,where\quad A\in\mathbb{R}^{n\times d},x\in\mathbb{R}^{d},b\in\mathbb{R}^n, \nonumber \\
	f(w) &= \frac{1}{m}\sum_{i=1}^m\log(1+\exp(-y_i\langle w,x_i\rangle)),where\quad y_i\in\{-1,1\},x_i\in\mathbb{R}^n,w\in\mathbb{R}^n.\nonumber
	\end{align}
\end{excercise}

\begin{PROOF}{e3}
bla.bla... bla bla.. bla.
\end{PROOF}

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