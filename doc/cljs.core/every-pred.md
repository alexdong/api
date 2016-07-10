---
name: cljs.core/every-pred
see also:
  - cljs.core/some-fn
  - cljs.core/and
---

## Signature
[p]
[p1 p2]
[p1 p2 p3]
[p1 p2 p3 & ps]


## Details

Takes a set of predicate functions and returns a function `f` that returns true
if all of its composing predicates return a logical true value against all of
its arguments, else it returns false.

Note that `f` is short-circuiting in that it will stop execution on the first
argument that triggers a logical false result against the original predicates.