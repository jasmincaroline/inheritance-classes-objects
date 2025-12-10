# Exercise 1 — Vehicle → Car
## Instructions
## 1 - Create a base class Vehicle with:

constructor(type)


method move() → logs "The {type} is moving."

## 2 - Create a subclass Car that:
calls super(type)
overrides move()
first calls super.move()
then logs "The {type} is driving fast."

## 3- Create a Car object and call .move().
Expected output pattern
The car is moving.
The car is driving fast.



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
## 1 - Create a class Person with:

constructor(name)


method greet() → "Hello, I am {name}."


## 2 - Create a child class Student:

calls super(name)


overrides greet()


calls super.greet()


logs "I am studying right now."


## 3 - Instantiate a Student and call greet().

## Expected output pattern
Hello, I am Maria.
I am studying right now.

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
Instructions
## 1 -  Class Appliance:
constructor(brand)
method turnOn() → "The {brand} appliance is now on."


## 2- Subclass Microwave:


calls super(brand)
overrides turnOn():


super.turnOn()


logs "The {brand} microwave is heating."


## 3 - Create a Microwave and call turnOn().


Expected output pattern
The Samsung appliance is now on.
The Samsung microwave is heating.
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
