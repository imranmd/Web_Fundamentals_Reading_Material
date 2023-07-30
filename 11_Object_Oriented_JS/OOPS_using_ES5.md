# Object-Oriented Programming (OOP) using ES5 in JavaScript

## Introduction to Object-Oriented Programming (OOP)

Object-Oriented Programming (OOP) is a programming paradigm that revolves around the concept of objects. An object is a self-contained unit that has properties (data) and methods (functions) that can operate on that data. OOP promotes the principles of encapsulation, inheritance, and polymorphism, allowing developers to create more modular and maintainable code. In this tutorial, we will explore OOP using ES5 (ECMAScript 5) in JavaScript, covering object creation, encapsulation, inheritance, and polymorphism.

## Object Creation

In ES5, object creation can be done using constructor functions. A constructor function is a regular function that is used with the `new` keyword to create objects.

```javascript
// Constructor function for creating Person objects
function Person(name, age) {
  this.name = name;
  this.age = age;

  this.greet = function () {
    return `Hello, my name is ${this.name}.`;
  };
}

// Creating Person objects using the constructor function
let person1 = new Person("John", 30);
let person2 = new Person("Jane", 25);

console.log(person1.greet()); // Output: "Hello, my name is John."
console.log(person2.greet()); // Output: "Hello, my name is Jane."
```

In the code snippet above, we created a constructor function `Person` that accepts `name` and `age` as parameters and initializes the object properties. The `greet` method is defined inside the constructor function and is available to all instances of `Person`.

## Encapsulation

Encapsulation is the idea of bundling data (properties) and methods (functions) that operate on that data within an object, preventing direct access to the internal state of the object from outside.

```javascript
function BankAccount(accountNumber, balance) {
  let accountNum = accountNumber; // Private property
  let acctBalance = balance; // Private property

  this.getBalance = function () {
    return acctBalance;
  };

  this.deposit = function (amount) {
    acctBalance += amount;
    return acctBalance;
  };

  this.withdraw = function (amount) {
    if (amount <= acctBalance) {
      acctBalance -= amount;
      return acctBalance;
    } else {
      return "Insufficient funds.";
    }
  };
}

let myAccount = new BankAccount("123456789", 1000);

console.log(myAccount.getBalance()); // Output: 1000

console.log(myAccount.accountNum); // Output: undefined (Private property)
console.log(myAccount.acctBalance); // Output: undefined (Private property)

myAccount.deposit(500);
console.log(myAccount.getBalance()); // Output: 1500

myAccount.withdraw(2000);
console.log(myAccount.getBalance()); // Output: "Insufficient funds."
```

In the example above, the `accountNum` and `acctBalance` variables are private properties, meaning they cannot be directly accessed from outside the `BankAccount` object. The methods `getBalance`, `deposit`, and `withdraw` provide controlled access to these private properties, ensuring data integrity and security.

## Inheritance

Inheritance is a fundamental concept in OOP that allows objects to inherit properties and methods from other objects. In ES5, inheritance can be achieved using the prototype chain.

```javascript
// Parent constructor function
function Animal(name) {
  this.name = name;
}

// Method in the parent's prototype
Animal.prototype.makeSound = function () {
  return "Unknown sound";
};

// Child constructor function
function Dog(name) {
  Animal.call(this, name); // Calling the parent constructor to initialize properties
}

// Inheriting from the parent's prototype
Dog.prototype = Object.create(Animal.prototype);

// Method in the child's prototype
Dog.prototype.makeSound = function () {
  return "Woof!";
};

// Creating objects
let animal = new Animal("Unknown");
let dog = new Dog("Buddy");

console.log(animal.name); // Output: "Unknown"
console.log(animal.makeSound()); // Output: "Unknown sound"

console.log(dog.name); // Output: "Buddy"
console.log(dog.makeSound()); // Output: "Woof!"
```

In the example above, we have a parent constructor function `Animal`, which has a method `makeSound` defined in its prototype. The child constructor function `Dog` inherits from `Animal` by setting its prototype to a new object created from `Animal.prototype`. This establishes a prototype chain, allowing `Dog` instances to inherit properties and methods from `Animal`.

## Polymorphism

Polymorphism allows objects of different types to be treated as if they are of the same type. In ES5, this can be achieved by having different objects with methods of the same name.

```javascript
function Shape() {
  this.getArea = function () {
    return "Unknown area";
  };
}

function Circle(radius) {
  this.radius = radius;
}

function Rectangle(width, height) {
  this.width = width;
  this.height = height;
}

Circle.prototype = Object.create(Shape.prototype);
Circle.prototype.getArea = function () {
  return Math.PI * this.radius ** 2;
};

Rectangle.prototype = Object.create(Shape.prototype);
Rectangle.prototype.getArea = function () {
  return this.width * this.height;
};

let shapes = [new Circle(5), new Rectangle(4, 6)];

shapes.forEach(function (shape) {
  console.log(shape.getArea());
});

// Output: 78.53981633974483 (Area of Circle with radius 5)
// Output: 24 (Area of Rectangle with width 4 and height 6)
```

In the example above, we have a parent constructor function `Shape` with a method `getArea`. The child constructor functions `Circle` and `Rectangle` inherit from `Shape` and override the `getArea` method with their own implementations. By using polymorphism, we can treat all the shapes in the array `shapes` as if they are of the same type (`Shape`) and call the `getArea` method, and the appropriate implementation will be executed based on the actual type of the object.

## Summary

ES5 provides powerful tools for implementing Object-Oriented Programming in JavaScript. By utilizing constructor functions and the prototype chain, we can create objects, encapsulate data, achieve inheritance, and leverage polymorphism. Understanding OOP in ES5 is fundamental to writing organized, modular, and maintainable code in JavaScript. As you delve deeper into JavaScript development, exploring these OOP concepts will enhance your ability to design and implement sophisticated applications. Happy coding!