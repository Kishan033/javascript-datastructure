# javascript-datastructure

## Basics

Total 7 kind of data types are available in javascript

[Boolean](https://choosealicense.com/licenses/mit/)

[Null](https://choosealicense.com/licenses/mit/)

[Undefined](https://choosealicense.com/licenses/mit/)

[Number](https://choosealicense.com/licenses/mit/)

[BigInt](https://choosealicense.com/licenses/mit/)

[String](https://choosealicense.com/licenses/mit/)

[Symbol](https://choosealicense.com/licenses/mit/)

[Object](https://choosealicense.com/licenses/mit/)

First 7 are primitives

All primitives are immutable, i.e., they cannot be altered. It is important not to confuse a primitive itself with a variable assigned a primitive value. The variable may be reassigned a new value, but the existing value can not be changed in the ways that objects, arrays, and functions can be altered.


## Boolean

Boolean represents a logical entity and can have two values: true and false.

0, -0, null, false, NaN, undefined and "" are considered as a falsy value.

Do not confuse the primitive Boolean values true and false with the true and false values of the Boolean object.

```
var variable = new Boolean(false);
if (variable) {
  // this code is executed
}
```

```
var variable = false;
if (variable) {
  // this code is not executed
}
```

```
var x = new Boolean(false);
if (x) {
  // this code is executed
}
```

Do not use a Boolean object to convert a non-boolean value to a boolean value. To perform this task, instead, use Boolean as a function, or a double NOT operator:

```
var x = Boolean(expression);
var x = !!(expression);
```
