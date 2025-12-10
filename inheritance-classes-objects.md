# Exercise 1 — Vehicle → Car
## Instructions
 1 - Create a base class Vehicle with:

constructor(type)


method move() → logs "The {type} is moving."

 2 - Create a subclass Car that:
calls super(type)
overrides move()
first calls super.move()
then logs "The {type} is driving fast."

 3 - Create a Car object and call .move().
Expected output pattern
The car is moving.
The car is driving fast.


## And... as Linus Torvalds said: "Show me the code":
```js
class Vehicle {
  constructor(type) {
    this.type = type;
  }

  move() {
    console.log(`The ${this.type} is moving.`);
  }
}

class Car extends Vehicle {
  constructor(type) {
    super(type);
  }

  move() {
    super.move();
    console.log(`The ${this.type} is driving fast.`);
  }
}

const myCar = new Car("car");
myCar.move();
```
<br>

# Exercise 2 — Person → Student
## Instructions
 1 - Create a class Person with:

constructor(name)


method greet() → "Hello, I am {name}."


 2 - Create a child class Student:

calls super(name)

overrides greet()

calls super.greet()
logs "I am studying right now."

3 - Instantiate a Student and call greet().
Expected output pattern
Hello, I am Maria.
I am studying right now.
----
## And... as Linus Torvalds said: "Show me the code":
```js
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello, I am ${this.name}.`);
  }
}

class Student extends Person {
  constructor(name) {
    super(name);
  }

  greet() {
    super.greet();
    console.log("I am studying right now.");
  }
}

const student = new Student("Maria");
student.greet();
```



# Exercise 3 — Appliance → Microwave
## Instructions
1 -  Class Appliance:
constructor(brand)
method turnOn() → "The {brand} appliance is now on."


2- Subclass Microwave:


calls super(brand)
overrides turnOn():
super.turnOn()
logs "The {brand} microwave is heating."


3 - Create a Microwave and call turnOn().


Expected output pattern
The Samsung appliance is now on.
The Samsung microwave is heating.
---
## And... as Linus Torvalds said: "Show me the code":

```js
class Appliance {
  constructor(brand) {
    this.brand = brand;
  }

  turnOn() {
    console.log(`The ${this.brand} appliance is now on.`);
  }
}

class Microwave extends Appliance {
  constructor(brand) {
    super(brand);
  }

  turnOn() {
    super.turnOn();
    console.log(`The ${this.brand} microwave is heating.`);
  }
}

const micro = new Microwave("Samsung");
micro.turnOn();
```



# Exercise 4 – Animal → Bird (new methods + extra property)

## Instructions
1 - Create a class Animal:
constructor(name)

method info() → logs:
 "This animal is called {name}."


2 -  Create a subclass Bird:
constructor(name, canFly)
calls super(name)
stores canFly (true/false)
overrides info():
first calls super.info()
then logs:
"It can fly." if canFly is true
"It cannot fly." if canFly is false
adds a new method sing():
logs: "🎵 {name} is singing."

3 -  Create two birds: 
---
One that can fly, e.g., "Eagle"
One that cannot fly, e.g., "Penguin"
Call info() and sing() for both.
Call **info()** and **sing()** for both.
-----
## And... as Linus Torvalds said: "Show me the code":
```js
class Animal {
  constructor(name) {
    this.name = name;
  }

  info() {
    console.log(`This animal is called ${this.name}.`);
  }
}

class Bird extends Animal {
  constructor(name, canFly) {
    super(name);
    this.canFly = canFly;
  }

  info() {
    super.info();
    if (this.canFly) {
      console.log("It can fly.");
    } else {
      console.log("It cannot fly.");
    }
  }

  sing() {
    console.log(`🎵 ${this.name} is singing.`);
  }
}

const eagle = new Bird("Eagle", true);
const penguin = new Bird("Penguin", false);

eagle.info();
penguin.info();
```
