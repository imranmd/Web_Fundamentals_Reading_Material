# Object-Oriented Programming (OOP) using ES6 in JavaScript

## Introduction to Object-Oriented Programming (OOP)

Object-Oriented Programming (OOP) is a programming paradigm that focuses on organizing code into self-contained objects. Each object has its own properties (data) and methods (functions) that operate on that data. ES6 (ECMAScript 2015) introduced several new features and syntax improvements that make Object-Oriented Programming in JavaScript more intuitive and concise. In this tutorial, we will explore OOP using ES6, covering object creation, encapsulation, inheritance, and polymorphism.

## Object Creation

In ES6, object creation can be done using classes and constructor functions. A class is a blueprint for creating objects, and the `constructor` method inside the class initializes the object properties.

```javascript
// ES6 Class for creating Person objects
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    return `Hello, my name is ${this.name}.`;
  }
}

// Creating Person objects using the class
let person1 = new Person("John", 30);
let person2 = new Person("Jane", 25);

console.log(person1.greet()); // Output: "Hello, my name is John."
console.log(person2.greet()); // Output: "Hello, my name is Jane."
```

In the code snippet above, we defined a class `Person` with a `constructor` method that initializes the `name` and `age` properties. The `greet` method is defined inside the class and is available to all instances of `Person`.

## Encapsulation

Encapsulation in ES6 is achieved using classes and private fields (using `#` notation). Private fields are not directly accessible outside the class, promoting data encapsulation.

```javascript
// ES6 Class for creating BankAccount objects
class BankAccount {
  #accountNum; // Private field
  #acctBalance; // Private field

  constructor(accountNumber, balance) {
    this.#accountNum = accountNumber;
    this.#acctBalance = balance;
  }

  getBalance() {
    return this.#acctBalance;
  }

  deposit(amount) {
    this.#acctBalance += amount;
    return this.#acctBalance;
  }

  withdraw(amount) {
    if (amount <= this.#acctBalance) {
      this.#acctBalance -= amount;
      return this.#acctBalance;
    } else {
      return "Insufficient funds.";
    }
  }
}

let myAccount = new BankAccount("123456789", 1000);

console.log(myAccount.getBalance()); // Output: 1000

console.log(myAccount.#accountNum); // Output: Error (Private field)
console.log(myAccount.#acctBalance); // Output: Error (Private field)

myAccount.deposit(500);
console.log(myAccount.getBalance()); // Output: 1500

myAccount.withdraw(2000);
console.log(myAccount.getBalance()); // Output: "Insufficient funds."
```

In the example above, we used private fields (`#accountNum` and `#acctBalance`) to encapsulate data within the `BankAccount` class. The private fields are not accessible from outside the class, ensuring data privacy and integrity.

## Inheritance

Inheritance in ES6 is achieved using the `extends` keyword to create a subclass (child class) that inherits from a superclass (parent class).

```javascript
// ES6 Class for the parent Animal
class Animal {
  constructor(name) {
    this.name = name;
  }

  makeSound() {
    return "Unknown sound";
  }
}

// ES6 Class for the child Dog inheriting from Animal
class Dog extends Animal {
  constructor(name) {
    super(name); // Calling the parent constructor to initialize properties
  }

  makeSound() {
    return "Woof!";
  }
}

// Creating objects
let animal = new Animal("Unknown");
let dog = new Dog("Buddy");

console.log(animal.name); // Output: "Unknown"
console.log(animal.makeSound()); // Output: "Unknown sound"

console.log(dog.name); // Output: "Buddy"
console.log(dog.makeSound()); // Output: "Woof!"
```

In the example above, we defined a parent class `Animal` and a child class `Dog` using the `extends` keyword. The `Dog` class inherits the properties and methods of the `Animal` class. The `super` keyword is used to call the parent class constructor and initialize the properties.

## Polymorphism

Polymorphism in ES6 is achieved by creating different classes with methods of the same name.

```javascript
// ES6 Class for Shape
class Shape {
  getArea() {
    return "Unknown area";
  }
}

// ES6 Class for Circle inheriting from Shape
class Circle extends Shape {
  constructor(radius) {
    super();
    this.radius = radius;
  }

  getArea() {
    return Math.PI * this.radius ** 2;
  }
}

// ES6 Class for Rectangle inheriting from Shape
class Rectangle extends Shape {
  constructor(width, height) {
    super();
    this.width = width;
    this.height = height;
  }

  getArea() {
    return this.width * this.height;
  }
}

let shapes = [new Circle(5), new Rectangle(4, 6)];

shapes.forEach((shape) => {
  console.log(shape.getArea());
});

// Output: 78.53981633974483 (Area of Circle with radius 5)
// Output: 24 (Area of Rectangle with width 4 and height 6)
```

In the example above, we have a parent class `Shape` with a `getArea` method. The child classes `Circle` and `Rectangle` inherit from `Shape` and override the `getArea` method with their own implementations. By using polymorphism, we can treat all the shapes in the array `shapes` as if they are of the same type (`Shape`) and call the `getArea` method, and the appropriate implementation will be executed based on the actual type of the object.

## Summary

ES6 introduced significant improvements to Object-Oriented Programming in JavaScript. By utilizing classes, constructor functions, and new syntax features, we can create objects, encapsulate data, achieve inheritance, and leverage polymorphism. Understanding OOP in ES6 is crucial for writing cleaner, more organized, and maintainable code in JavaScript. As you advance in JavaScript development, exploring these OOP concepts will empower you to design and implement complex applications with ease. Happy coding!