---
layout: default
title: 4-Solutions
nav_order: 5
parent: Workshop Activities
---

# Solution to Activity 3
If you and your group have any questions, or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Have fun!

Note: Please insert the **\usepackage{amsmath}** after `\documentclass[a4paper,12pt]{article}` and above the \begin{document}. Type the following codes into your main body, which means that these codes should be included into \begin{document}.

```
\section{Simple math equations}
The square root of 5: $\sqrt{5}$.\\
The ratio of the circumference of a circle to its diameter: $\pi$.\\
\emph{My first integral} $\int \zeta^{2}(x) dx$
\[\sqrt{a^{2} + b^{2}}\]
To type a fraction:
\[\frac{3+x}{y+z}\]

If the sub/superscript contains more than one character, it should be enclosed in curly braces, as in $100^{x+y}$, $X_{ij}$.\\

The commands for Greek letters are easy and intuitive: $\alpha,\beta,\gamma,\lambda,\Gamma,\Lambda$

Align the equations:

\begin{align*}
  f(x) &= x^2\\
  g(x) &= \frac{1}{x}\\
  h(x) &= \int^a_b \frac{1}{3}x^3 dx
\end{align*}

To get a matrix,
\[
[\begin{matrix}
1 & 0\\
0 & 1
\end{matrix}
\]

We can find that the plain [ ] symbols do not scale as the matrix grows. To fix this, we use the following code:
\[
\left[\begin{matrix}
1 & 0\\
0 & 1
\end{matrix}\right]
\]

It can be used to scale large fractions and other expressions:
\[\left(\frac{3+x}{y+z}\right)\]

Type the following equations in Latex:
\[
\frac{1 + \int_0^\pi \cos x dx}{
x+y+xy}
\]

\[
f'(a)=\lim_{x \to a} \frac{f(x) - f(a)}{x - a}
\]

\[(x+y)^n=\sum_{k=0}^n\binom{n}{k}x^{n-k}y^k\]
\[
\begin{vmatrix}
a+b+c&
uv\\
a+b&c+d
\end{vmatrix}
=7
\]

Align two or more formulas:
\begin{align}
1 &= \cos^{2} x + \sin^{2} x                    \label{E:eqn1}\\
\prod^n_{j=1}
\hat x_{j} &=\tan^{-1}(z-2)                     \label{E:eqn2}\\
y_{ij}&=\mu+\tau_i+\beta_j+\epsilon_{ij}        \label{E:anova}
\end{align}

(Refer equations) Equation~\ref{E:anova} is the model for ANOVA.

Cases:
\[
H[n]=
\begin{cases}
0,        &\text{if $n < 0$,}\\
\frac {1}{2},    &\text{if $n=0$,}\\
0,        &\text{if $n=0$,}
\end{cases}
\]

Type the following chemical equations. Firstly, you need to import a package called ``mhchem". Type ``$\backslash$usepackage[version=3]\{mhchem\}" in preamble.
\paragraph{Isotopes} \ce{^{227}_{90}Th+}, \ce{NO3-}, \ce{1/2H2O}

\paragraph{easy} \ce{SO4^2- + Ba^2+ -> BaSO4 v}, \ce{CO2 + C ->[\alpha][\beta] 2CO}

\paragraph{hard}\ce{Zn^2+ <=>[\ce{+ 2OH-}][\ce{+ 2H+}] $\underset{\text{amphoteres Hydroxid}}{\ce{Zn(OH)2 v}}$ <=>C[+2OH-][{+ 2H+}] $\underset{\text{Hydroxozikat}}
{\cf{[Zn(OH)4]^2-}}$}
```

[NEXT STEP: Presentations With Beamer](act-5.html){: .btn .btn-blue }
