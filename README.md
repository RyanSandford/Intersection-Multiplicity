# Intersection-Multiplicity
This Project was used to get familiar with the Maple programming Language and learn the intricacies of intersection
multiplicity in the bi-variate case.

__Note:__ .mw files will not be properly displayed on github, it is recommended to download and open them elsewhere.

__Multiplicity.mw__ implements Fulton's Algorithm to compute the intersection multiplicity for bivariate polynomials
in an algebraically closed field, where the gcd of the input polynomials has degree 1.
Conditions (2-1) - (2-7) referenced in both the algorithm and implementation are listed below.

__(2-1)__ I(p; f , g) is a non-negative integer for any C, D, and p such that C
      and D have no common component at p. We set I(p; f , g) = ∞ if C
      and D have a common component at p.
__(2-2)__ I(p; f , g) = 0 if and only if p ∈/ C ∩ D.
__(2-3)__ I(p; f , g) is invariant under affine change of coordinates on A^2
__(2-4)__ I(p; f , g) = I(p; g, f )
__(2-5)__ I(p; f , g) is greater or equal to the product of the multiplicity of p
      in f and g, with equality occurring if and only if C and D have no
      tangent lines in common at p.
__(2-6)__ I(p; f , gh) = I(p; f , g) + I(p; f , h) for all h ∈ k[x, y].
__(2-7)__ I(p; f , g) = I(p; f , g + hf ) for all h ∈ k[x, y].


__Multiplicity_Single.mw__ can be used with the above implementation of Fulton's Algorithm to extend to the case 
where one of the input polynomials is zero. In this case the intersection multiplicity is defined to be m+1 where
the m is such that the mth partial derivative is the smallest order which evaluates to a non-zero number on p=(a,b).

__Multiplicity_Single.mw__ can also work on polynomials in K[x] by pasing [x, 0] into the arguement vars.
Similarly it will work for univariate polynomials in K[y] by passing [0, y] into the arguement vars.
Lastly to ensure compatiability with the above implementation of Fulton's Algorithm the input polynomial
f must still be defined on both x and y, hence f: (x,y) -> K.
