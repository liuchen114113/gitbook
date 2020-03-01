# this指向的改变
<!-- toc -->

- [1、call](#1、call)
- [2、apply](#2、apply)
- [3、bind](#3、bind)

<!-- tocstop -->

## 1、**call**
```
Function.prototype.call = function (target, ...args) {
  var context = target || window
  context.fn = this
  var result = context.fn(...args)
  delete context.fn
  return result
}
```
## 2、**apply**
```
Function.prototype.apply = function (target, args) {
    var context = target
    context.fn = this
    let result = args && args.length ? context.fn(...args) : context.fn()
    delete context.fn
    return result
}
```
## 3、**bind**
```
Function.prototype.bind = function (target, args) {
    let _this = this
    return function () {
        let context = target
        context.fn = _this
        let res = args && args.length ? context.fn(...args) : context.fn()
        delete context.fn
        return res
    }
}
```