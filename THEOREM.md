# Theorem (three-chain Jacobian rank)

**Author:** Benjamin Stanley Frohman  
**Copyright:** © 2026 Benjamin Stanley Frohman  
**License:** Apache-2.0

## Statement

Let

```text
W = u^5 v + v^6
F = W(x0, x3) + W(x1, x4) + W(x2, x5)
    = x0^5 x3 + x3^6 + x1^5 x4 + x4^6 + x2^5 x5 + x5^6
```

in `C[x0,...,x5]`, and let `J(F) = C[x0,...,x5] / (∂F)`. Let `R_k` be the degree-`k` summand. Let `X = V(F) ⊂ P^5` and `Π = V(x3, x4, x5)`.

Then:

1. The only common zero of the six partial derivatives is the origin. Hence `X` is a smooth sextic fourfold, and those partials are a regular sequence of degree `5`.
2. `dim J(F) = 5^6 = 15625`. The same integer is `25^3`, because `J(F)` is the tensor product of three copies of `J(W)` and `dim J(W) = 25`.
3. The Hilbert series is

```text
sum_k (dim R_k) t^k = (1 + t + t^2 + t^3 + t^4)^6.
```

4. Griffiths residue gives the primitive Hodge numbers of any smooth sextic, and therefore of this one:

```text
dim R_0  = 1    = h^{4,0}
dim R_6  = 426  = h^{3,1}
dim R_12 = 1751 = h^{2,2}_prim
dim R_18 = 426  = h^{1,3}
dim R_24 = 1    = h^{0,4}
```

Lefschetz adds the class `h^2`, so `h^{2,2}(X) = 1752` and `b_4(X) = 2606`.

5. `F` vanishes on `Π`, so `X` lies on the Noether–Lefschetz locus of sextics that contain a plane. None of the integers `dim R_k` changes because of that. They are the same integers as for a very general smooth sextic.

## Proof

**Isolation.** The partials split by pairs:

```text
∂F/∂x0 = 5 x0^4 x3,     ∂F/∂x3 = x0^5 + 6 x3^5,
```

and likewise for `(x1,x4)` and `(x2,x5)`. On one block `W = u^5 v + v^6` the Jacobian ideal contains `v^6`, `u^5`, and `u^4 v` (Euler in characteristic `0` puts `v^6` in the ideal). The only solution of `5 u^4 v = 0` and `u^5 + 6 v^5 = 0` is `u = v = 0`. The three pairs use disjoint variables, so the only common zero of `∂F` is the origin. A hypersurface in `P^5` whose affine cone is singular only at the origin is smooth.

**Dimension.** Six homogeneous forms of degree `5` in six variables, with common zero only at the origin, form a regular sequence. The Hilbert series of the quotient is

```text
(1 - t^5)^6 / (1 - t)^6 = (1 + t + t^2 + t^3 + t^4)^6.
```

Evaluating at `t = 1` is illegitimate in that form; the substitution `1 + t + ... + t^4` at `t = 1` gives `5^6 = 15625`.

**Tensor product.** A monomial basis of `J(W)` is

```text
{1, u, u^2, u^3} × {1, v, ..., v^5}  ∪  {u^4},
```

which has `4·6 + 1 = 25` elements. Leading terms `v^6`, `u^5`, `u^4 v` cut the `5 × 6` rectangle of `30` monomials by five, and `30 - 5 = 25`. Disjoint variables give

```text
J(F) ≅ J(W) ⊗ J(W) ⊗ J(W),     dim = 25^3 = 15625.
```

**Hodge numbers.** For a smooth hypersurface of degree `6` in `P^5`, Griffiths' residue isomorphism identifies

```text
H^{4-p, p}_prim(X) ≅ R_{6p}.
```

The coefficient of `t^12` in `(1 + t + t^2 + t^3 + t^4)^6` is `1751`. Primitive `H^2` vanishes by the Lefschetz hyperplane theorem, so

```text
H^4(X) = P^4(X) ⊕ C·h^2,     h^{2,2} = 1751 + 1 = 1752.
```

**Independence of the plane.** The series depends only on the degree of the partials and on the regular-sequence hypothesis. Both are shared with every smooth sextic. Vanishing of `F` on `Π` is an extra geometric fact. It is not an extra relation in the Jacobian ideal, and it does not change `dim R_k`.

## What the theorem is not

It is not a computation of

```text
ρ_Hdg(X) = dim ( H^4(X, Q) ∩ H^{2,2}(X) ).
```

That integer satisfies `2 ≤ ρ_Hdg(X) ≤ 1752`. The lower bound is `rank Q⟨h^2, [Π]⟩ = 2`, from the intersection matrix

```text
[  6  1 ]
[  1 21 ]     determinant 125.
```

The upper bound is `h^{2,2}`. The Jacobian ring computes the upper bound's complex ambient dimension. It does not compute the rational subspace.

In particular this theorem does not assert `ρ_Hdg = 3`, does not produce a class outside `Q⟨h^2, [Π]⟩`, and does not prove that the image of the cycle-class map equals that span. Those three claims are the Hodge problem on this host. They are not this theorem.

The Fermat sextic has rational Hodge rank `1752` by a separate argument about Fermat monomials. That argument does not apply to a sum of three chains.

## The question that is settled

**Question.** For this special member of the Noether–Lefschetz locus, is the graded Jacobian rank different from the rank of a very general sextic?

**Answer.** No. Every `dim R_k` agrees. The speciality is invisible to the Jacobian rank and can appear only in the rational Hodge rank, which is not a graded piece of `J(F)`.
