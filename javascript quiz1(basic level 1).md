1. What is JavaScript?
> JavaScript is a high-level, interpreted programming language primarily used for creating interactive web pages and web applications. It runs in web browsers and enables dynamic content, user interactions, and client-side scripting. It can also be used on the server-side with environments like Node.js.

2. What is the difference between b/w let and var?
 > var is function-scoped (accessible throughout the entire function), while let is block-scoped (accessible only within the block, such as inside {})
   if (true) {
      var a = 10;
       let b = 20;
    }
   console.log(a); // Works
   console.log(b); // Error
 > var declarations hoisted to top of their scope and initialized with undefined,allowing use before declaration. let is hoisted but not initialized, causing a ReferenceError if accessed before declaration.
    console.log(a); // undefined
    var a = 10;
    console.log(b); // Error
    let b = 10;
 > var allows redeclaration in the same scope, while let does not.
  var x = 5;
  var x = 10; //Allowed
  let y = 5;
  let y = 10; // Error
 > var creates a property on the global object , but  let does not 


3. Why do we prefer const over var?
> const make code sefer, clearer ,& less error-prone. means no accidental changes like: 1--> const means values can't be reassigned.  2--> var can chang any time which cause bugs
Eg:-
       const a = 10;
       a = 20; //error

       var b = 10;
       b = 20; //allowed


4. What is the use of javascript in web browsers?
 > JavaScript is used in web browsers to make websites interactive and dynamic (not just static pages).
 >interactive:-
        button.onclick = function() {
          alert("Button clicked!");
        };

 >Update content without reloading page:-
        document.getElementById("text").innerHTML = "Hello!";

 >Form validation:-
        if (password.length < 6) {
          alert("Password too short");
        }

 >Communicate with server (API calls):-
       fetch("api/data")
         .then(res => res.json())
         .then(data => console.log(data));

5. What are Objects?
> object stores related information together and it represent real-world things
   const person = {
      name: "Shubham",
      age: 22,
      city: "Jaipur"
    };

6. What is an array and how is it different from an Object in Javascript?
> An array is a special type of object used to store multiple values in a single variable
   const fruits = ["apple", "banana", "mango"];
>object stores related information together
  const person = {
      name: "Shubham",
      age: 22,
      city: "Jaipur"
    };

7. What is a function?
> A function is a block of code that performs a specific task and can be reused whenever needed.
  function add(a, b) {
    return a + b;
  }
  console.log(add(2, 3)); 

8. How can we implement call by value and call by reference in Javascript?
> 1. Call by Value (Primitive Data Types)
- A copy of the value is passed to the function
- Changes inside function do NOT affect original value
:-    function changeValue(x) {
       x = 20;
      }
     let a = 10;
     changeValue(a);
     console.log(a); // 10 (no change)

> 2. Call by Reference (Objects & Arrays)
- The reference (address) is passed
- Changes inside function affect original value
   function changeObject(obj) {
     obj.name = "Rahul";
    }
    let person = { name: "Shubham" };
    changeObject(person);
    console.log(person.name); // Rahul (changed)
  
9. What are the primitive data types in Javascript?
 > Primitive data types in JavaScript are basic data types that store single values, including Number, String, Boolean, Undefined, Null, BigInt, and Symbol.

10. What is DOM?
>  Document Object Mode is a tree-like structure of your HTML page that JavaScript can control
 -HTML:-  <body>
            <h1>Hello</h1>
            <p>Welcome</p>
          </body>
 DOM structure: 
        body
         ├── h1 → "Hello"
         └── p  → "Welcome"

11. Why do we need DOM?
  > We need the DOM so that JavaScript can access, modify, and update the content, structure, and style of a webpage dynamically, making it interactive.








// Programs 

1. Average of array nums in Javascript?

 function findAvg(nums){
    let sum =0;
    for (let i=0;i < nums.length; i++){
        sum+=nums[i];
    }
    return sum/nums.length;
 }
 console.log(findAvg([1,2,3,4,5]))



2. Swap two numbers by reference?
  function swap(obj){
    let temp=obj.a;
    obj.a=obj.b;
    obj.b=temp;
  }
  letnums={a:10, b: 20};
  swap(nums);
  console.log(numbers.a, numbers.b);


3. Print the fibonacci sequence?
  function printFibonacci(n) {
    let a = 0, b = 1;
    for (let i = 0; i < n; i++) {
       console.log(a);
       let next = a + b;
       a = b;
       b = next;
    }
  }
  printFibonacci(7);


4. Sort an array by both ascending and descending order?
  a. Ascending Order
     let arr = [5, 2, 9, 1, 3];
     arr.sort((a, b) => a - b);
     console.log(arr);
 
  b. Descending Order
     let arr = [5, 2, 9, 1, 3];
     arr.sort((a, b) => b - a);
     console.log(arr); // [9, 5, 3, 2, 1]


5. Show a variable value in an HTML webpage using DOM?
 > We use the DOM to display a JavaScript variable inside an HTML element.

   HTML:-
     <!DOCTYPE html>
     <html>
       <body>
         <h1 id="demo"></h1>
         <script src="script.js"></script>
       </body>
    </html>
    JavaScript:
      let message = "Hello Shubham!";
     document.getElementById("demo").innerHTML = message;

     Output :- Hello Shubham!





 