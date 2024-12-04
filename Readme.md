1. What are Anonymous Functions in JavaScript?
Anonymous functions are functions that do not have a name. They are often used as arguments to other functions or assigned to variables.
Example:
let greet = function() {
    console.log("Hello, World!");
};
greet(); // Output: Hello, World!

2. Explain Strict Comparison and Abstract Comparison in JavaScript?
Strict Comparison (===):
Compares both value and type. No type conversion is performed.
Example:
console.log(5 === '5'); 
console.log(5 === 5);  

Abstract Comparison (==):
Compares only values after performing type conversion (type coercion).
Example:
console.log(5 == '5'); 
console.log(0 == false);


4. What is Hoisting in JavaScript?
Hoisting is a behavior where variable and function declarations are moved to the top of their containing scope during the compile phase.
Example:
console.log(a); // undefined
var a = 5;
greet(); // "Hello!"
function greet() {
    console.log("Hello!");
}

5. JavaScript is a Garbage Collected Programming Language, Explain How?
JavaScript uses an automatic garbage collection mechanism to manage memory. The garbage collector periodically identifies and removes objects that are no longer accessible or used (unreachable).
Mechanism:
If an object has no references or is unreachable from the global execution context, it becomes eligible for garbage collection.

6. Explain Shallow Copy vs Deep Copy in JavaScript?
Shallow Copy:
Creates a new object but only copies references for nested objects. Changes to nested objects in the copy affect the original.
Example:
let obj1 = { a: 1, b: { c: 2 } };
let shallowCopy = { ...obj1 };
shallowCopy.b.c = 3;
console.log(obj1.b.c); // 3

Deep Copy:
Copies all levels of an object, creating independent nested objects.
Changes to the copy do not affect the original.
Example:
let obj1 = { a: 1, b: { c: 2 } };
let deepCopy = JSON.parse(JSON.stringify(obj1));
deepCopy.b.c = 3;
console.log(obj1.b.c); // 2

7. What is Object.freeze in JavaScript?
Object.freeze() is a method that prevents modifications to an object's properties. It prevents the addition of new properties, deletion of existing properties, and modification of existing properties.
Example:
const obj = { a: 1, b: 2 };
Object.freeze(obj);
obj.a = 3; // Fails silently in non-strict mode or throws error in strict mode
delete obj.b; // Throws an error
obj.c = 4; // Fails silently

Projects:

1. Write a function that generates a random number between two ranges, -100 to 0 and 800 - 900.
          function generateRandomNumber() {
          const rangeSelector = Math.random() < 0.5 ? 'first' : 'second';
          if (rangeSelector === 'first') {
            return Math.floor(Math.random() * 101) - 100;
          } else {
            return Math.floor(Math.random() * 101) + 800;
          }
        }
            const randomNumber = generateRandomNumber();
            console.log(randomNumber);
