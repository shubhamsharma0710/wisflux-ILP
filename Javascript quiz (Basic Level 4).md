1. What are anonymous functions in JavaScript?
>An anonymous function is a function without a name, often used as a callback or assigned to a variable for short-term use.

2. Explain strict comparison and Abstract comparison in javascript?
>Abstract comparison (==) compares values after type conversion, while strict comparison (===) compares both value and type without conversion, making it safer and more predictable.
console.log(5 === "5");  // false
console.log(5 === 5);    // true
&
console.log(5 === "5");  // false
console.log(5 === 5);    // true

3. Difference b/w arrow functions and regular functions?
>Arrow functions have shorter syntax and lexical this, while regular functions have their own this, support arguments, and can be used as constructors.
>Regular function
function add(a, b) {
  return a + b;
}
>Arrow function
const add = (a, b) => a + b;


4. What is Hoisting in JavaScript?
>variables/functions can be used before they are declared
>variable hosting
console.log(a); // undefined
var a = 10;
>function hosting
greet(); // ✅ Works
function greet() {
  console.log("Hello!");
}


5. JavaScript is a garbage collected programming language, explain how?
>JavaScript is a garbage collected language because it automatically manages memory by removing objects that are no longer reachable using algorithms like mark-and-sweep.
function test() {
  let a = 10;
}
test();
// 'a' is destroyed after function ends

6. Explain Shallow copy vs Deep copy in Javascript?
>Shallow copy copies only the first level and shares references of nested objects, while deep copy creates a completely independent copy of all levels, preventing changes from affecting the original.
>shallow copy
let obj1 = {
  name: "Shubham",
  address: { city: "Jaipur" }
};
let obj2 = { ...obj1 }; // shallow copy
obj2.address.city = "Delhi";
console.log(obj1.address.city); // Delhi (changed)
>Deep copy
let obj1 = {
  name: "Shubham",
  address: { city: "Jaipur" }
};
let obj2 = structuredClone(obj1); // deep copy
obj2.address.city = "Delhi";
console.log(obj1.address.city); // Jaipur (unchanged)

7. What is Object.freeze?
>Object.freeze() is used to make an object immutable by preventing addition, deletion, or modification of its properties, though it works only at the top level (shallow).
const obj = {
  name: "Shubham",
  age: 22
};
Object.freeze(obj);
obj.name = "Rahul";  //  not allowed
obj.city = "Jaipur"; //  not allowed
delete obj.age;      //  not allowed
console.log(obj); // { name: "Shubham", age: 22 }