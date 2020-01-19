# Javascript Datatypes
JavaScript variables can hold many data types: numbers, strings, objects and more:

**Primitive (Value Type)** Store in STACK
- Number
- Boolean
- String
- Null
- Undefined
- Symbol
- BigInt 

**Non Primitive (Reference Type)** Store in HEAP
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

#### More deep on the topic

##### Primitive Example
```javascript
var name = 'Suryansh'
console.log(name)

var secondName = name;
console.log(secondName)

name = 'Anita'
console.log(secondName)

// Suryansh
// Suryansh
// Suryansh
```

##### Non Primitive Example
```javascript
var person = {
    age: 28,
    name: 'Suryansh',
    hobbies: ['Coding', 'Dancing']
}
console.log(person)

var secondPerson = person
console.log(secondPerson)

person.name = 'Ravish'
console.log(secondPerson)
// {age: 28, name: "Suryansh", hobbies: Array(2)}
// {age: 28, name: "Suryansh", hobbies: Array(2)}
// {age: 28, name: "Ravish", hobbies: Array(2)}
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
- https://www.w3schools.com/js/js_datatypes.asp
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof
- https://www.youtube.com/watch?v=9ooYYRLdg_g
