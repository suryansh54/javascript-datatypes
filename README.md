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
console.log([] == []) // false (looks identical here it doesn't make it identical still two different objects two different places in the heap.)
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

#### Additional Knowledge
##### Difference Between Stack and the heap
- Both Stack and Heap are stored in RAM.
- Variable allocation is fast on stack where as on heap its slow.
- Variables on stack go out of scope automatically once their need is done. That means de-allocation on stack is automatic. On heap, in regards to C and C++ we have to manually de-allocate where as high-level languages such as Java has garbage collection schemes.
- On stack, we can access variables without the need for pointers and hence its fast and that is the reason it is used to store local data, method arguments and the call stack etc all that which needs less amount of memory.
- You would use stack only when you know for sure how much memory for your data you would need even before compile time. On the other hand, we can use heap without us having to know for sure the amount of memory we need.

Stack | Heap 
--- | --- 
Memory allocated from stack is called static memory allocation. | Memory allocated from Heap is called dynamic memory allocation.
Stack is very fast access time's point of view. | Heap has slower access time than stack.
Limited stack size is given to a program for its execution and it is OS-dependent. | Size of Heap is not limited to the program the way stack is. A program can allocate as much memory dynamically as needed until heap exhasted

#### Reference:
- https://www.w3schools.com/js/js_datatypes.asp
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof
- https://www.youtube.com/watch?v=9ooYYRLdg_g
- https://www.quora.com/What-is-the-difference-between-the-stack-and-the-heap
