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

## Null

The value null represents the intentional absence of any object value. It is one of JavaScript's primitive values and is treated as falsy for boolean operations.

null expresses a lack of identification, indicating that a variable points to no object.

## Undefined

undefined is a property of the global object. That is, it is a variable in global scope.
Since EcmaScript 5, it is specified as non-writable.

1)A variable that has not been assigned a value is of type undefined. 2)
A function returns undefined if a value was not returned.

## Null vs Undefined
undefined means a variable has been declared but has not yet been assigned a value
null is an assignment value. It can be assigned to a variable as a representation of no value
undefined is a type itself (undefined) while null is an object

## Number

The Number type is a 64-bit binary format value. It is able to represent floating-point numbers.

It has total three Symbolic value
```+Infinity```, ```-Infinity```, ```NaN```.

To check limit ```Number.MAX_SAFE_INTEGER``` and ```Number.MIN_SAFE_INTEGER```.

To check safety of number ```Number.isSafeInteger()```
