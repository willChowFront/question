**readme上是已解决的问题及答案，issue上是未解决的问题**

# question

##binding.html
`var unboundSlice = Array.prototype.slice,
slice = Function.prototype.call.bind(unboundSlice);
console.log(slice({'0':'la','1':'lala2','2':'lala3',length:3}));`
没有理解这段代码的原因在于，没有仔细看MDN上的call的解释，.bind()将unboundSlice设置为call函数中的this，call中的this值指向当前调用对象
**A different this object can be assigned when calling an existing function. this refers to the current object, the calling object.**

##bindPolyfill.html
###问题
1.`this instanceof fNOP && oThis ? this : oThis`的作用
2.`fNOP.prototype = this.prototype;fBound.prototype = new fNOP();`的作用



