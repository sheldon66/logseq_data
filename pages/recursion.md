---
title: recursion
---

## recursion
:PROPERTIES:
:id: 6077ac46-b21f-47d1-9603-235be6052de9
:END:
## tail recursion
###
```sml
(* recursion *)
fun fact n = if n=0 then 1 else n*fact(n-1)

(* tail recursion *)
fun fact n = 
	let fun aux (n, acc) = 
    	if n=0
        then acc
        else aux(n-1, acc*n)
	in aux(n,1)
  	end
```