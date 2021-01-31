---
title: pattern matching
---

## precise definition
pattern `p` value `v`
1. variable `x`: `x -> v`
2. _ : match succeeds and no bindings
3. (p1, ... pn) matches (v1, ..., vn)
4. p is C p1 , V is C v1 (the sate constructor)
### function pattern
```
fun (a, b) = 1
|
```
