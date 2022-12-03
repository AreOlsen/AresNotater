# Computing powers of a number recursively.

Although most programming languages have a built in power function we can make one recursively as long as the exponent is an integer.

Suppose we want to compute $x^n$ if $n==0$ then the value is $1$. This is a good basecase.
## Math.
When you multiply the powers of $x$ you add the exponents for any base of $x$ and exponents $a,b$. $x^a\times x^b=x^{a+b}$. Therefore if $n$ is positive and even $x^n=x^{\frac{n}{2}}\times x^{\frac{n}{2}}$. If you want to compute $y=x^{\frac{n}{2}}$ [[Rekurisve algoritmer.|recursion]] you could compute $x^n=y\times y$ . If $n$ is positive and odd however then $x^n=x^{n-1}\times x$. Therefore you could compute $x^{n-1}$ recursively, and then use this to compute $x^n=x^{n-1}\times x$. When $n$ is negative , then $x^n=\frac{1}{x^{-n}}$. The exponent $-n$ becomes positive and you can compute this recursively, and take its reciprocal. 


## Psuedocode.
Putting the follow observations together we get the following recursive algorithm for computing $x^n$.

1. The base case is when $n==0$ and $x^0=1$.
2. If $n$ is positive and even recursively compute $y=x^{\frac{n}{2}}$. And then $x^n=y\times y$.
	1. Notice you only have to do one recursive call here computing $x^{\frac{n}{2}}$ just once and then multiplying it by itself.
3. If $n$ is positive and odd recursively compute $x^{n-1}$. So that the exponent is either positive and even or $0$. Then $x^n=x^{n-1}\times x$.
4. If $n$ is negative recursively compute $x^{-n}$ so that the exponent and then $x^n=\frac{1}{x^{-n}}$.

