---
sidebar_position: 1
---


- Object oriented programming is programming paradigm based on the concepts of objects.

- We use object to model real world or abstract features.

## Classes and Instances

- Classes is like a blueprint that use to create new objects.


## Four Fundamental OOP principals

- Abstaction

- Encapsulation

- Inheritence

- Polymorphism

**1) Abstaction**

- It means ignoring or hiding details that doesn't matter, allowing us to get an overview perspective of thing we are implementing, instead of messing with details that really don't matter to our implementation.

**2) Encapsulation**

- Keeping properties and method  private inside the class, so they are not accessible outside the  class. Some methods can be exposed as a public interface(API).

**3) Inheritance**

- Making all properties and methods of a certain class available to child class, forming a hierarchical relationship between classes. This allows us to reuse common logic and to model real-world relationships.

**4) Polymorphism**

- A child class can overwrite a method it inherited from a parent class.


## OOP in JavaScript

- OOP in JavaScript is prototype. Objects are link to certain prototype object. Prototype object contains methods and properties that all the object linked to that prototype can access and used. This is know as prototypal inheritance.

## 3 Ways of implementing Prototypal inheritance in JavaScript

**1) Constructor functions**

- Technique to create objects from a function.
- This is how built-in objects like Arrays,Maps or Sets are actually implemented.

**2) ES6 Classes**

- ES6 classes work exactly like constructor functions.
- Modern way to write OOP in JavaScript.

3) Object.create()

- The easiest and most straightforward way of linking an object to a prototype object.