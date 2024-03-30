# Character Theory of the Symmetric Group via Sage
Jupyter notebook to construct character tables of symmetric groups by recursively inducing characters from subgroups.

Warning: During this whole document, we assume that the characteristic of the field over which we consider representations is relatively prime to the order of the finite group in consideration. Modular representations are much more complicated to deal with.

## Short description:
The representation theory of symmetric groups is completely understood in terms of the combinatorics of Young diagrams. However the character table of the nth symmetric group can be calculated inductively using the following procedure.

0) Assume that all character tables for the ith symmetric group for all i less than n are known.
1) First induce the characters of the ith symmetric group for all i less than n under the natural embedding of Si into Sn.
2) Then induce the characters of all the Young subgroups of the nth symmetric group. I.e., Use embeddings Si x Sj into  Sn where the sum of i and j is at most n.
3) Use Orthogonality relations between characters to decompose the induced characters in steps 2 and 3 into irreducible representations (This is the non-deterministic part. Can we prove that Young subgroups are always enough to fill the full character table of S_n?)

The sage worksheet builds tools to induce and lift characters from scratch and can be modified per user need. 

Notes: 
1) Since the character table of the symmetric groups can be integrally realized, there is no loss of precision in calculations.
2) This technique can be adapted to bootstrap the character table of the alternating groups via the restriction action and using Frobenius reciprocity. (If you've already done this, please let me know!)
3) I plan to use this to further implement a constructive version of the Artin-Wedderburn theorem for symmetric groups, i.e. obtain a decomposition of the groupring of the symmetric group into matrix rings over division algebras.

If you have any similar ideas/improvements, please contact me!
