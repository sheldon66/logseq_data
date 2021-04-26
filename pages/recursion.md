---
title: recursion
---

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