# fourier transform of [...]

The following is the correct version of a calculation appearing in the note "qkz.pdf" thanks to Allen Knutson's comments.

## "should agree with" -> "should be leading-order behavior of”

in the context of the example..it works!

The example was $V = \{$upper-triangular $3 \times 3$ square zero matrices$\}$. For the component $X = \{a = 0\}$, i.e. matrices of the form

$$
\begin{pmatrix}
0 & 0 & b \\
 & 0 & c \\
 &   & 0
\end{pmatrix}
$$
the coordinate ring $\mathbb{C}[X]$ has character

$$
\sum_{(i,j)} e^{(z_1,z_2,z_3)\cdot (-i,-j,i+j)} \dim \mathbb{C}\{b^i,c^j\}
$$
since $t = \text{diag}(t_1,t_2,t_3)$ in $GL(3)$ acts on the *entries* $b$ and $c$ by $t_1/t_3$ and $t_2/t_3$ respectively, i.e. with weights $(1,0,-1)$ and $(0,1,-1)$.

Expanding we get

$$
\begin{aligned}
\text{ch} \mathbb{C}[X] &= \sum_{(i,j)} e^{-iz_1 -jz_2 + (i+j)z_3} \\
               &= \sum_i e^{-i(z_1 - z_3)} \sum_j e^{-j(z_2 - z_3)} \\
               &= \frac{1}{1-e^{z_1-z_3}} \frac{1}{1-e^{z_2-z_3}}
\end{aligned}
$$
whose Laurent series near zero has leading order term

$$
\frac{1}{z_1-z_3}\frac{1}{z_2-z_3}
$$
like we want!

Re 4.2 yes, in a component worth of preprojective modules we insist that maps up (xor down) be zero but I still have no idea what the “core” is.