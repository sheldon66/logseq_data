---
title: Object create
---

### new操作符
:PROPERTIES:
:language: javascript
:END:
#### new 操作符做了哪些步骤
:PROPERTIES:
:id: 60867ca2-b97e-492d-b31d-819bbbef0c77
:END:
当一个函数被使用 new 操作符执行时，它按照以下步骤：
1. 一个新的空对象被创建并分配给 this。
2. 函数体执行。通常它会修改 this，为其添加新的属性。
3. 返回 this 的值。

#+BEGIN_QUOTE
https://zh.javascript.info/constructor-new
#+END_QUOTE
### click
:PROPERTIES:
:type: ((6077ac46-f040-4368-9898-ab338af20bac))
:END: