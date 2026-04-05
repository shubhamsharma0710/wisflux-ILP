1. Explain as much as you know about objects in javascript? (A long answer expected).
>Objects in JavaScript are collections of key-value pairs used to represent real-world entities. They are dynamic, can store properties and methods, support nesting, and are reference types, making them essential for structuring and managing data in applications.

2. Read the code :
// This is an object based vector template
var vector = {
_x: 0,
_y: 0,
create: function(x,y){
var obj = Object.create(this);
obj.setX(x);
obj.setY(y);
return obj;
},
}
Can you make a “class” based alternative to it? Using Javascript OOP features.


>class Vector {
  constructor(x, y) {
    this._x = x;
    this._y = y;
  }

  setX(x) {
    this._x = x;
  }

  setY(y) {
    this._y = y;
  }

  getX() {
    return this._x;
  }

  getY() {
    return this._y;
  }

  static create(x, y) {
    return new Vector(x, y);
  }
}

3. Do you think javascript is the language of the future?
>Yes, JavaScript is considered a language of the future because it runs on multiple platforms, has a huge ecosystem, high demand, and continues to evolve with modern technologies.


//programs

1. Write code implementations of arr methods -
a. forEach
b. map
c. filter
d. reduce
e. includes
f. some
g. every

> a. forEach()
Array.prototype.myForEach = function(callback) {
  for (let i = 0; i < this.length; i++) {
    callback(this[i], i, this);
  }
};
>  b. map()
Array.prototype.myMap = function(callback) {
  let result = [];
  for (let i = 0; i < this.length; i++) {
    result.push(callback(this[i], i, this));
  }
  return result;
};

>c. filter()
Array.prototype.myFilter = function(callback) {
  let result = [];
  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) {
      result.push(this[i]);
    }
  }
  return result;
};

>d. reduce()
Array.prototype.myReduce = function(callback, initialValue) {
  let acc = initialValue;
  let start = 0;
  if (acc === undefined) {
    acc = this[0];
    start = 1;
  }
  for (let i = start; i < this.length; i++) {
    acc = callback(acc, this[i], i, this);
  }
  return acc;
};

>e. includes()
Array.prototype.myIncludes = function(value) {
  for (let i = 0; i < this.length; i++) {
    if (this[i] === value) {
      return true;
    }
  }
  return false;
};

>f. some()
Array.prototype.mySome = function(callback) {
  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) {
      return true;
    }
  }
  return false;
};

>g. every()
Array.prototype.myEvery = function(callback) {
  for (let i = 0; i < this.length; i++) {
    if (!callback(this[i], i, this)) {
      return false;
    }
  }
  return true;
};

3. To do list task
/* you have to arrays
1. ToDo
2. Completed
! implement three functions
1. add(title)
2. remove(id)
3. update(id, title)
4. markAsCompleted(id)
* The ToDo array is a list of tasks (object)
each task has an id (number) and a title (string)
* eg :
{id: 1, task: 'Learn JavaScript'}
Implementation
1. add function will add a task to the ToDO array with an unique
id
- it will accept a title as a string and return the id of the
new task
- it will return -1 if the title is empty
2. remove function will remove a task from the TODO array
- it will accept an id as a number and return true if the
task was removed
- it will return false if the id is not found
3. update function will update the title of a task
- it will accept an id as a number and a title as a string
- it will return true if the task was updated
- it will return false if the id is not found
4. markAsCompleted will remove a task from the TODO array and add
it to the Completed array
- it will accept an id as a number and return true if the
task has been moved
- it will return false if the id is not found

> example
let id1 = add("Learn JavaScript");
let id2 = add("Practice DSA");

console.log(todo);

update(id1, "Learn JS Basics");

markAsCompleted(id2);

remove(id1);

console.log("Todo:", todo);
console.log("Completed:", completed);




