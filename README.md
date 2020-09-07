# Intersection-Multiplicity
This Project was used to get familiar with the Maple programming Language and learn the intricacies of intersection
multiplicity in the bi-variate case.

__Note:__ .mw files will not be properly displayed on github, it is recommended to download and open them elsewhere.

__Multiplicity.mw__ implements Fulton's Algorithm to compute the intersection multiplicity for bivariate polynomials
in an algebraically closed field, where the gcd of the input polynomials has degree 1.
Conditions (2-1) - (2-7) referenced in both the algorithm and implementation are listed below.

- __(2-1)__ I(p; f , g) is a non-negative integer for any C, D, and p such that C
      and D have no common component at p. We set I(p; f , g) = ∞ if C
      and D have a common component at p.
- __(2-2)__ I(p; f , g) = 0 if and only if p ∈/ C ∩ D.
- __(2-3)__ I(p; f , g) is invariant under affine change of coordinates on A^2
- __(2-4)__ I(p; f , g) = I(p; g, f )
- __(2-5)__ I(p; f , g) is greater or equal to the product of the multiplicity of p
      in f and g, with equality occurring if and only if C and D have no
      tangent lines in common at p.
- __(2-6)__ I(p; f , gh) = I(p; f , g) + I(p; f , h) for all h ∈ k[x, y].
- __(2-7)__ I(p; f , g) = I(p; f , g + hf ) for all h ∈ k[x, y].
