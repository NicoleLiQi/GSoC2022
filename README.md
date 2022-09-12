# GSoC2022

## Project Overview
This project intends to improve the `RealSet` algorithm and implement `PiecewisePolynomial` for general purposes for SageMath. Considering the computational complexity, an efficient piece searching algorithm should also be designed, especially for the case of a large number of pieces being provided. 

At the end of the project, we implemented the piecewise function in real set . It is still in progress to adjust to the SageMath Module Element structure. SageMath now can calctute and plot function as following:

```
sage: R.<t> = QQ[]
age: f1 = 1 - t
sage: f2 = t^2 - t
sage: D1 = RealSet((0, 1), [4, 5])
sage: D2 = RealSet((1, 2), [6, 7])
sage: p = PiecewisePolynomial([[D1, f1], [D2, f2]]); p
PiecewisePolynomial(t |--> -t + 1 on (0, 1) ∪ [4, 5], t |--> t^2 - t on (1, 2) ∪ [6, 7]; t)
sage: p.plot()
```

## List of Contribution
- [#32181](https://trac.sagemath.org/ticket/32181) Improve the scan-line algrothim for RealSet 
- [#34456](https://trac.sagemath.org/ticket/34456) Implement the piecewise polynomial on one dimension. Still working in progress to adpat the Module Element.

## Roadblocks encountered
- Trac-Server was more complicated than expectation. I experienced permission denied all the time throughout GSoC
- It was not easy to adapt the suitable format of docstring and doctest while implementing.
- In the implementation process, the balance between code readability and efficiency turns out to be difficult.

## TODO
- Adapt Vector Space for piecewise polynomial
- Implement multi variable piecewise polynomial

## Get Code
- Meta Ticket [#20877](https://trac.sagemath.org/ticket/20877) on SageMath Trac-Servece

