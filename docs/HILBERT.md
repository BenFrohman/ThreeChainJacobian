# Hilbert function of J(F)

**Author:** Benjamin Stanley Frohman  
**Copyright:** © 2026 Benjamin Stanley Frohman  
**License:** Apache-2.0

```text
sum_k (dim R_k) t^k = (1 + t + t^2 + t^3 + t^4)^6
```

Total dimension `15625`. Socle in degree `24`. The function is symmetric: `dim R_k = dim R_{24-k}`.

| k | dim R_k | k | dim R_k |
|---:|---:|---:|---:|
| 0 | 1 | 13 | 1686 |
| 1 | 6 | 14 | 1506 |
| 2 | 21 | 15 | 1246 |
| 3 | 56 | 16 | 951 |
| 4 | 126 | 17 | 666 |
| 5 | 246 | 18 | 426 |
| 6 | 426 | 19 | 246 |
| 7 | 666 | 20 | 126 |
| 8 | 951 | 21 | 56 |
| 9 | 1246 | 22 | 21 |
| 10 | 1506 | 23 | 6 |
| 11 | 1686 | 24 | 1 |
| 12 | 1751 | | |

Hodge reading, valid for every smooth sextic and therefore for this `F`:

| piece | value | source |
|---|---:|---|
| `h^{4,0}` | 1 | `R_0` |
| `h^{3,1}` | 426 | `R_6` |
| `h^{2,2}_prim` | 1751 | `R_12` |
| `h^{2,2}` | 1752 | primitive plus `h^2` |
| `h^{1,3}` | 426 | `R_18` |
| `h^{0,4}` | 1 | `R_24` |
| `b_4` | 2606 | sum of the Hodge numbers of `H^4` |

`dim R_12 = 1751` is not `ρ_Hdg`.
