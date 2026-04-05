1. Why do we use functions in JavaScript?
 > Functions are used to make code reusable, organized, and efficient.

2. What is Function Invocation?
> Function invocation means calling or executing a function.
   function greet() {
     console.log("Hello!");
    }
   greet(); // Function Invocation

3. Does a function behave like an object in Javascript? Prove it by an example
> yes function behave like objects in js.
> in js , function are first-class object, whivh mean they can have properties,methods,it passed as arguments,it also returned from other functions.
   function greet(name) {
     return "Hello " + name;
    }
    //  Adding property (like object)
    greet.language = "English";
    // Adding method (like object)
    greet.sayBye = function() {
      console.log("Bye!");
    };
    // Passing function as argument
    function execute(fn) {
      console.log(fn("Shubham"));
    }
    //Returning function from another function
    function outer() {
      return greet;
    }
    // Access property
    console.log(greet.language); // English
    // Call method
    greet.sayBye(); // Bye!
   // Pass function
   execute(greet); // Hello Shubham
  // Return & call function
  let newFunc = outer();
  console.log(newFunc("Rahul")); // Hello Rahul
  // Using built-in method (call)
   greet.call(null, "Aman"); // Hello Aman


4. What are Events in Javascript?
> Events are actions or occurrences that happen in the browser, which JavaScript can detect and respond to.
    document.getElementById("btn").onclick = function() {
       alert("Button clicked!");
    };

5. What is a string?
> A string is a data type used to store text (characters)
   let name = "Shubham";

6. What is an array? Is it static or dynamic in Javascript?
> An array is a data structure used to store multiple values in a single variable.
 > in js arrays are dynamic. so they can change anytime & add and remove element easily.
   let arr = [1, 2, 3];
   arr.push(4);   // add element
   arr.pop();     // remove last element
   console.log(arr); // [1, 2, 3]

7. Difference between Map and Set?
>  Map stores data in key-value pairs(like objects)
   let map = new Map();
   map.set("name", "Shubham");
   map.set("age", 22);
   console.log(map.get("name"));

> Set stores only unique values(no duplicates)
  let set = new Set();
  set.add(1);
  set.add(2);
  set.add(2); // duplicate
  console.log(set); // {1, 2}

8. Difference between Array and Map?
   > Array:-Stores ordered list of values
      let arr = ["apple", "banana", "mango"];
      console.log(arr[0]); // apple
  > Map:- Stores key–value pairs;
     let map = new Map();
     map.set("name", "Shubham");
     map.set("age", 22);
     console.log(map.get("name")); // Shubham

9. What are array methods? List a few names?  
>Array methods are built-in functions that help us perform operations on arrays like adding, removing, searching, or transforming data. example - push(), pop(), shift(), unshift(), map() etc

10. In how many ways can we traverse through an array in Javascript?
> We can traverse an array in JavaScript using multiple ways such as for loop, while loop, for...of, forEach(), map(), and for...in.


// programs

1. Reverse an array? Input: [1, 2, 3, 4, 5, 6]
  let arr = [1, 2, 3, 4, 5, 6];
  arr.reverse();
  console.log(arr); 

2. Explain the properties of the join array method function via program?
> The join() method is used to convert an array into a string by joining all elements.
  let arr = [1, 2, 3];
  let result = arr.join();
  console.log(result); // "1,2,3"

3. Show all the values of an array in a html webpage using DOM and forEach method?
  js : 
  let arr = [1, 2, 3, 4, 5];
  let ul = document.getElementById("list");
  arr.forEach(function(value) {
     let li = document.createElement("li"); // create <li>
      li.textContent = value;               // add value
      ul.appendChild(li);                  // add to <ul>
    });


4. Merge to sets in javascript? (hint use Set class in javascript)

  let set1 = new Set([1, 2, 3]);
  let set2 = new Set([3, 4, 5]);
  let mergedSet = new Set([...set1, ...set2]);
  console.log(mergedSet); // {1, 2, 3, 4, 5}