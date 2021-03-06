# javascript-datastructure

## Basics

Total 7 kind of data types are available in javascript

[Boolean](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#boolean)

[Null](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#null)

[Undefined](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#undefined)

[Number](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#number)

[BigInt](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#bigInt)

[String](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#string)

[Symbol](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#symbol)

[Object](https://github.com/Kishan033/javascript-datastructure/blob/master/README.md#object)

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

## String

With BigInts, you can safely store and operate on large integers even beyond the safe integer limit for Numbers.

A BigInt is created by appending n to the end of an integer or by calling the constructor.

```const x = 2 ** 53```

It has total three Symbolic value
```+Infinity```, ```-Infinity```, ```NaN```.

To check limit ```Number.MAX_SAFE_INTEGER``` and ```Number.MIN_SAFE_INTEGER```.

To check safety of number ```Number.isSafeInteger()```

BigInts cannot be operated on interchangeably with Numbers. TypeError will be thrown.

## String

JavaScript's String type is used to represent textual data. It is a set of "elements" of 16-bit unsigned integer values.

Unlike some programming languages (such as C), JavaScript strings are immutable. This means that once a string is created, it is not possible to modify it.

## Symbol

A “symbol” represents a unique identifier.

A value of this type can be created using ```Symbol()```.

```let id = Symbol();```

With description
```let id = Symbol("id");```


Symbols are guaranteed to be unique. Even if we create many symbols with the same description, they are different values. The description is just a label that doesn’t affect anything.
```
let id1 = Symbol("id");
let id2 = Symbol("id");
id1 == id2;
```

Symbols don’t auto-convert to a string

```alert(id)```

#### Hidden properties
Symbols allow us to create “hidden” properties of an object, that no other part of code can accidentally access or overwrite.

```
let user = { // belongs to another code
  name: "John"
};
let id = Symbol("id");
user[id] = 1;
user[id];
```

#### Symbols are skipped by most of iterators
```
let id = Symbol("id");
let user = {
  name: "John",
  age: 30,
  [id]: 123
};

for (let key in user) alert(key);
```

#### Global symbols
```
// read from the global registry
let id = Symbol.for("id"); // if the symbol did not exist, it is created

// read it again (maybe from another part of the code)
let idAgain = Symbol.for("id");

// the same symbol
alert( id === idAgain ); // true
```

#### Symbol.keyFor
```
let globalSymbol = Symbol.for("name");
let localSymbol = Symbol("name");

alert( Symbol.keyFor(globalSymbol) ); // name, global symbol
alert( Symbol.keyFor(localSymbol) ); // undefined, not global

alert( localSymbol.description ); // name
```

## Objects

In JavaScript, objects can be seen as a collection of properties.

Property values can be values of any type, including other objects, which enables building complex data structures. Properties are identified using key values. A key value is either a String or a Symbol value.

#### JSON Vs Object
JSON is a data interchange format. It's a standard which describes how ordered lists and unordered maps, strings booleans and numbers can be represented in a string. Just like XML and YAML

A JavaScript object on the other hand is a physical type. Just like a PHP array, a C++ class/ struct, a JavaScript object is an type internal to JavaScript.

#### Functions
Functions are regular objects with the additional capability of being callable.

#### Dates
Global date object is also derived from object.

#### Arrays
Arrays are regular objects for which there is a particular relationship between integer-key-ed properties and the length property.

Additionally, arrays inherit from Array.prototype, which provides to them a handful of convenient methods to manipulate arrays.

#### Map
Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.

```
let map = new Map();

map.set('1', 'str1');   // a string key
map.set(1, 'num1');     // a numeric key
map.set(true, 'bool1'); // a boolean key
```
Difference

1)Any keys, objects can be keys.

2)Additional convenient methods, the size property.

#### Set
A Set is a special type collection – “set of values” (without keys), where each value may occur only once.

To create set ```new Set(iterable)``` .

```
let set = new Set();

set.add(1);
set.add(1);
console.log(set);
```

Methods like add, delete, has, clear, size

For complex data structure refer https://github.com/trekhleb/javascript-algorithms
