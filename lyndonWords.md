# lyndon words

```GAP
irreducible characters:
IC[1] = (q+q^-1)[1|2|2|3]+[1|2|3|2]+[2|1|2|3], 
IC[2] = [2|1|3|2]+[2|3|1|2], 
IC[3] = [2|1|2|3]+(q+q^-1)[2|2|1|3]+(q+q^-1)[2|2|3|1]+[2|3|2|1],
IC[4] = [1|2|3|2]+(q+q^-1)[1|3|2|2]+(q+q^-1)[3|1|2|2]+[3|2|1|2], 
IC[5] = [2|3|2|1]+[3|2|1|2]+(q+q^-1)[3|2|2|1]

goodwords:
[ 2, 1, 2, 3 ],
[ 2, 3, 1, 2 ],
[ 2, 3, 2, 1 ],
[ 3, 2, 1, 2 ],
[ 3, 2, 2, 1 ]

polytopes:
conv(1, 1+2, 1+2+2, 1+2+3, 2, hw)
conv(2, 1+2, 1+2+3, 2+3, hw)
conv(2, 1+2, 1+2+2, 2+2, 2+2+3, 2+3, hw)
conv(1, 1+2, 1+2+3, 1+3,3, 2+3, hw)
conv(2, 2+3, 2+2+3, 3, 1+2+3, hw)

mv cycles:
?
?
?
?
?

equivariant multiplicities:
?
?
?
?
?
```

## questions

1. Since $\alpha_1 + 2\alpha_2 + \alpha_3$ is the "normalized form" of $2\omega_2$, these (equivalent) lists should fit into $\mathcal B(2\omega_2)$ for $A_3$ but $\mathcal B(2\omega_2)$ has cardinality 20.
1. What are goodwords and do they uniquely determine their irreducible characters?
1. These shuffle characters clearly do determine certain MV polytopes. What is the precise question we are posing?

## todo

1. implement polytope(goodword)
1. implement lusztig_datum(polytope)

I would like to know if it’s possible to recover Pol(Z) from eqm(Z), mdeg(Z) or the torus multigraded Hilbert series of C[Z]. If these shuffle characters biject with dual semicanonical basis, and match Hilb C[Z], then I guess the answer is no. The counterexample from our appendix k

For example 

```
IC[1]
=
(q^3+3*q+3*q^-1+q^-3)[1|2|2|3|3|4|4|5]+
         (q^2+2+q^-2)[1|2|2|3|3|4|5|4]+
         (q^2+2+q^-2)[1|2|2|3|4|3|4|5]+
             (q+q^-1)[1|2|2|3|4|3|5|4]+
             (q+q^-1)[1|2|2|3|4|5|3|4]+
         (q^2+2+q^-2)[1|2|3|2|3|4|4|5]+
             (q+q^-1)[1|2|3|2|3|4|5|4]+
             (q+q^-1)[1|2|3|2|4|3|4|5]+
                     [1|2|3|2|4|3|5|4]+
                     [1|2|3|2|4|5|3|4]+
             (q+q^-1)[1|2|3|4|2|3|4|5]+
                     [1|2|3|4|2|3|5|4]+
                     [1|2|3|4|2|5|3|4]+
                     [1|2|3|4|5|2|3|4]+
         (q^2+2+q^-2)[2|1|2|3|3|4|4|5]+
             (q+q^-1)[2|1|2|3|3|4|5|4]+
             (q+q^-1)[2|1|2|3|4|3|4|5]+
                     [2|1|2|3|4|3|5|4]+
 		     [2|1|2|3|4|5|3|4]+
	     (q+q^-1)[2|1|3|2|3|4|4|5]+
		     [2|1|3|2|3|4|5|4]+
                     [2|1|3|2|4|3|4|5]+
                     [2|1|3|4|2|3|4|5]+
             (q+q^-1)[2|3|1|2|3|4|4|5]+
                     [2|3|1|2|3|4|5|4]+
                     [2|3|1|2|4|3|4|5]+
                     [2|3|1|4|2|3|4|5]+
                     [2|3|4|1|2|3|4|5]
```
<!-- 
Observation: The last term is ’the’ good word [2|3|4|1|2|3|4|5].

Questions: 

The polytope P_L of this module is the convex hull of \sum_1^j \alpha_{i_j} (j\le k) for those strings i = (i_1..i_k) such that e_i L \ne 0. Obviously each of these words defines the same point \alpha = 12221 to abuse notation. The point is that all truncations of all these words will also define points in P_L? -->