# Three-chain Jacobian rank

**Author:** Benjamin Stanley Frohman  
**Copyright:** © 2026 Benjamin Stanley Frohman  
**License:** Apache-2.0  
**Status:** public

This repository records one theorem about one polynomial. It is not a proof or a disproof of the Hodge conjecture, and it does not compute the rational Hodge rank of the sextic.

## The polynomial

```text
F = x0^5 x3 + x3^6 + x1^5 x4 + x4^6 + x2^5 x5 + x5^6
W = u^5 v + v^6
F = W(x0,x3) + W(x1,x4) + W(x2,x5)
```

`X = V(F)` is a hypersurface in `P^5`.

## The question this closes

Does the plane on `X` change the graded dimension of the Jacobian ring, relative to a very general smooth sextic?

**No.**

That is the statement proved here. It is a different problem from

```text
ρ_Hdg = dim ( H^4(X,Q) ∩ H^{2,2}(X) ).
```

The Jacobian calculation does not see that rational subspace.

## Theorem

See [THEOREM.md](THEOREM.md). Short form:

1. The only common zero of `∂F` is the origin, so `X` is smooth.
2. `dim J(F) = 5^6 = 25^3 = 15625`.
3. The Hilbert function is `(1 + t + t^2 + t^3 + t^4)^6`, the same series as for every smooth sextic in `P^5`.
4. In particular `dim R_12 = 1751`, so `h^{2,2}(X) = 1752` after adding the hyperplane square.
5. Containment of the plane `Π = V(x3,x4,x5)` changes none of these numbers.

## What stays open

```text
2 ≤ ρ_Hdg(X) ≤ 1752.
```

The lower bound is the rank of `Q⟨h^2, [Π]⟩` (intersection determinant `125`). The upper bound is `h^{2,2}`. Neither the equality `ρ_Hdg = 2` nor a jump past `2` follows from `dim R_12`.

## Files

| path | contents |
|---|---|
| [THEOREM.md](THEOREM.md) | statement, proof, and the separation from Hodge |
| [docs/HILBERT.md](docs/HILBERT.md) | full Hilbert function |
| [LICENSE](LICENSE) | Apache-2.0 |
