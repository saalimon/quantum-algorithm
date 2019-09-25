# quantum-algorithm
implement Shor's algorithm without quantum part ,this shor's algorithm (classical computing) implemented by using python3 <br>
=== Classical part ===<br>
<ol>
  <li>Pick a random number a<N /li>
  <li>Find gcd(a,N) = 1 mod(N)</li>
  <li>Find r by brute-force (can use period-finding subroutine in quantum-part/quantum fourier transform)</li>
  <li>find p and q by using p = gcd(a^(r/2)-1,N) and q = gcd(a^(r/2)+1,N)</li>
</ol>



