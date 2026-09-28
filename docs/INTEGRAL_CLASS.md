# Integral class on the three-chain sextic

**Author:** Benjamin Stanley Frohman  
**Copyright:** © 2026 Benjamin Stanley Frohman  
**License:** Apache-2.0

The Jacobian rank computed in this repository is neither the rational Hodge rank nor an integral cycle class. This file only records the integral combination forced by the plane.

```text
α = [Π] − (1/6) h^2          rational, primitive, not an integral class
β = 6α = h^2 − 6[Π] = [S] − 5[Π]
```

`β` is integral, orthogonal to `h^2`, and an integral combination of surfaces. It lies in the image of `CH^2(X) → H^4(X,Z)`. It is not a counterexample to the integral Hodge conjecture.

The integral Hodge conjecture is a different sentence from the rational one, and it is already false on other varieties (Atiyah–Hirzebruch; Kollár). See `BenFrohman/HODGE-DISPROOF/docs/INTEGRAL_HODGE.md`.

The lattice `Z h^2 + Z[Π]` has discriminant `125`. Saturation in `H^4(X,Z)` is not decided here. The graded Jacobian calculation does not see it.
