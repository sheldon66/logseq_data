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
```
