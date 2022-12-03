# $\text{Big } \theta$   / Big theta - notation.

## Linear search.

The worst case time complexity of a linear search is the input size "n". Each iteration it has to do several things, and these things has a a computation time.
The computation time is dependant on the computer and other factors such as programming language. 

In addition other computations may be present that are not dependant on input size.
We cant note the compelexity as $C_1 \times n + C_2$. Where $C_1$ is the comptutation time dependant on the input size and $C_2$ is the computation time not dependant on the input size. 

The running time of all these computations is called $\theta(n)$ "Theta of n". 
We say that at the best the running time is $K_1\times n$, and at worst $K_2 \times n$.
For some values of $K$.

Once n gets very large we say that the running time has to be inbetween $K_1\times n$ and $K_2 \times n$

>[!Note]
>$\theta(n)$ is not restricted to just input of n, it can be any function of n.
>For example: $\theta(n\times \log(n))$. 

## Some more general knowledge.
When using Big $\theta$ we say we have an asymptotically tight bound on the running time. 
"Asymptotically" as it only matters for big values of $n$. And "tight bound" as it lies between the best scenario and worst.

A visual guide to Big $\theta$:
![](https://qph.fs.quoracdn.net/main-qimg-fbe65e88a496258c5de9ab25555f0508)



 Functions in asymptotic notation when the best case scenario is at the first position of n, we say that the algorithm has a complexity of $\theta(n^0)$ aka. $\theta(1)$.


Now say that for example it takes $\theta(\log_{10}(n))$ you could also say that is takes $\theta(\log_{2}(n))$ whenever the base of the $\log$ is a constant, we can have it whatever we please. As we have a mathematical proof that is as follows:
$\log_a(n)=\frac{\log_b(n)}{\log_b(a)}$ . And as we discussed earlier in [[Asymptotic notation.]] we do not care for coefficients, we can indeed set the base to whatever we want. For all positive values of $a,b,n$. If $a\space \& \space b$ are  constants they differ only by a value of $\log_b(a)$, which is a factor so we ignore it.  For example the worst running time of binary search is $\log_a(n).$ Because at most it would be $\log_b(n)+1$. Because they are constants we can also say that it is just $\log_a(n)$. 

>[!Funny note]
>Normally computer scientists like to use $\log_2(n)$, because we like to think in base 2. 😂


There is often an order to the functions we say when analyzing using asymptotic notation. If $a\lt b$, then $\theta(n^a)$ grows slower than $\theta(n^b)$.

Example:
$n^1$ grows slower than $n^2$. 

The exponents do not have to be integers either.
Logarithms grow slower than polynomials, $\theta(\log_2(n))$ grows slower than $\theta(n)$, but $\theta(1)$ is the fastest!

Often encountered speeds:
1. $\theta(1)$
2. $\theta(\log_2(n))$
3. $\theta(n)$
4. $\theta(n\times \log_2(n))$
5. $\theta(n^2)$
6. $\theta(n^2 \times \log_2(n))$
7. $\theta(n^3)$
8. $\theta(2^n)$
9. $\theta(n!)$

>[!Note.]
>$a^n$ always grows faster than $n^b$ when b is constant and $a\lt1$.
