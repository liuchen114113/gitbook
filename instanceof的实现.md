# instanceof的实现
```
function myInstanceof(left, right) {
    while (left !== null) {
        if (left.__proto__ === right.prototype) {
            return true
        } else {
            left = left.__proto__
        }
    }
    return false
}
```