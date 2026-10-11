---
created: 2026-10-11 14:18
modified: 2026-10-11 14:44
---
# Pade Approximants
https://www.youtube.com/watch?v=szMaPkJEMrw - Youtube Explanation:
- Default Taylor Series Centered at $x=c$: $$f(x)\approx \sum_{n=0}^{\infty}\frac{f^n(x-c)x^n}{n!}$$
- A Pade Approximant is an approximation of a function using rational polynomials
- A $\frac{N}{M}$ Pade approximant is formed like so $$P^N_{M}(x)\approx\frac{\sum_{i=0}^NA_{i}x^i}{\sum_{j=0}^MB_{j}x^j}$$
- Taylor Series tend to dissapate rather quickly without doing larger term approximations
- https://onlinelibrary.wiley.com/doi/10.1155/2020/2753691 
- This paper talks about refinements in pade approximations for trig functions, and introduces the notion of a maximum error
- This mettric  is the maximum error between a function and its upper bound, and the maximum error between a function and its lower bound
- It compares these metrics and finds that the pade approximation is superior to the taylor approximation
- It doesn't however, mention anything about the relative computational speed of these approxximations
