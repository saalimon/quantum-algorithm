# quantum-algorithm
implement Shor's algorithm without quantum part ,this shor's algorithm (classical computing) implemented by using python3
Pick a random number {\displaystyle a<N}{\displaystyle a<N}.
Compute {\displaystyle \gcd(a,N)}{\displaystyle \gcd(a,N)}, the greatest common divisor of {\displaystyle a}a and {\displaystyle N}N. This may be done using the Euclidean algorithm.
If {\displaystyle \gcd(a,N)\neq 1}{\displaystyle \gcd(a,N)\neq 1}, then this number is a nontrivial factor of {\displaystyle N}N, so we are done.
Otherwise, use the quantum period-finding subroutine (below) to find {\displaystyle r}r, which denotes the period of the following function:
{\displaystyle f(x)=a^{x}{\bmod {N}}.}{\displaystyle f(x)=a^{x}{\bmod {N}}.}
This is the order {\displaystyle r}r of {\displaystyle a}a in the group {\displaystyle (\mathbb {Z} _{N})^{\times }}{\displaystyle (\mathbb {Z} _{N})^{\times }}, which is the smallest positive integer {\displaystyle r}r for which {\displaystyle f(x+r)=f(x)}{\displaystyle f(x+r)=f(x)}, or {\displaystyle f(x+r)=a^{x+r}{\bmod {N}}\equiv a^{x}{\bmod {N}}}{\displaystyle f(x+r)=a^{x+r}{\bmod {N}}\equiv a^{x}{\bmod {N}}}. By Euler's Theorem, {\displaystyle r}r divides {\displaystyle \varphi (N)}{\displaystyle \varphi (N)}, where {\displaystyle \varphi }\varphi  denotes Euler's totient function.
If {\displaystyle r}r is odd, then go back to step 1.
If {\displaystyle a^{r/2}\equiv -1({\bmod {N}})}{\displaystyle a^{r/2}\equiv -1({\bmod {N}})}, then go back to step 1.
Otherwise, at least one of {\displaystyle \gcd(a^{r/2}+1,N)}{\displaystyle \gcd(a^{r/2}+1,N)} and {\displaystyle \gcd(a^{r/2}-1,N)}{\displaystyle \gcd(a^{r/2}-1,N)} is a nontrivial factor of {\displaystyle N}N, so we are done.
