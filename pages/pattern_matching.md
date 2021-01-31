---
title: patter matching
---

## nested pattern
```sml
(* 
zip3([1,2,3],[4,5,6],[7,8,9]);
val it = [(1,4,7),(2,5,8),(3,6,9)] : (int * int * int) list 
*)

fun zip3 list_triple =
    case list_triple of 
	([],[],[]) => []
      | (hd1::tl1,hd2::tl2,hd3::tl3) => (hd1,hd2,hd3)::zip3(tl1,tl2,tl3)
      | _ => raise ListLengthMismatch
      
fun unzip3 lst =
    case lst of
	[] => ([],[],[])
      | (a,b,c)::tl => let val (l1,l2,l3) = unzip3 tl
		       in
			   (a::l1,b::l2,c::l3)
		       end
               
fun nondecreasing xs =
    case xs of
	[] => true
      | x::[] => true
      | head::(neck::rest) => (head <= neck andalso nondecreasing (neck::rest))
```
