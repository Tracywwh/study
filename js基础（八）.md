this：

在非严格模式下：总是指向一个对象；
在严格模式下：可以是任意值。

eg：
function f2(){
  return this
}
f2() === window => true 非严格模式下，指向window

function g2(){
  'use strict'
   return this
}
g2() === undefined => true 严格模式下，如果this没有被执行环境定义，那它将保持为undefined


*this的值从一个环境传到另一个，就要用call和apply方法
call(obj,参数1,参数2) obj直接替代函数中的this对象，后者(多个元素)作为参数传递给被调用的函数
apply(obj,[参数1,参数2]) obj直接替换函数中的this对象，后者是数组。


eg:
let arr = [1,4,34,23,1,4,54,77]
let max = Math.max.apply(null,arr)  => 77 
数组不能进行Math.max()，使用apply就可以操作了





