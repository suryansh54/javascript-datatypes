# Javascript Datatypes
JavaScript variables can hold many data types: numbers, strings, objects and more:

**Primitive (Value Type)**
- Number
- Boolean
- String
- Null
- Undefined
- Symbol
- BigInt 

**Non Primitive (Reference Type)**
- Array
- Object
- Function
- Date
- Regex

```javascript
function isPrimitive(test) {
    return (test !== Object(test));
};

// Not Primitive
isPrimitive([]) // false
isPrimitive({}) // false
isPrimitive(new Number(100)); // false
console.log([] == []) // false
console.log([1] == [1]) // false
console.log({} == {}) // false

// Primitive
isPrimitive(100); // true
isPrimitive("Suryansh") // true
isPrimitive(true) // true
isPrimitive(false) // true
isPrimitive(undefined) // true
isPrimitive(null) // true
```

### Expressions - typeof
The typeof operator returns a string indicating the type of the unevaluated operand.

| Type | Result |
| --- | --- |
| Undefined | "undefined" |
| Null | "object" |
| Boolean | "boolean" |
| Number | "number" |
| BigInt | "bigint" |
| String | "string" |
| Symbol | "symbol" |
| Function | "function" |
| Any other object | "object" |

```javascript
console.log(typeof 42);
// expected output: "number"

console.log(typeof 'blubber');
// expected output: "string"

console.log(typeof true);
// expected output: "boolean"

console.log(typeof undeclaredVariable);
// expected output: "undefined";
```

#### Reference:
https://www.w3schools.com/js/js_datatypes.asp
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof
