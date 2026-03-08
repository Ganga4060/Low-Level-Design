# Inheritance

## What is Inheritance?

Inheritance is an **Object-Oriented Programming (OOP)** concept where one class can **acquire the properties and behaviors of another class**.

In simple words:

> Inheritance allows a class to reuse the code of another class.

The class that provides the properties is called the **Parent (Base) Class**, and the class that receives them is called the **Child (Derived) Class**.

---

## Simple Real Life Example

Think about a **family**.

A child inherits many features from their parents like:

- Eye color  
- Hair color  
- Height  

Similarly in programming, a **child class inherits properties and methods from a parent class**.

Example relationship:

```
Animal → Dog
```

A dog is an animal, so it can use the common features of animals.

---

## Basic Example (C++)

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    void eat() {
        cout << "Animal is eating" << endl;
    }
};

class Dog : public Animal {
public:
    void bark() {
        cout << "Dog is barking" << endl;
    }
};

int main() {
    Dog d;

    d.eat();   // inherited from Animal
    d.bark();  // Dog's own method
}
```

### Output

```
Animal is eating
Dog is barking
```

### Explanation

- **Animal** → Parent Class  
- **Dog** → Child Class  

`Dog` inherits the `eat()` function from `Animal`.

---

## Syntax of Inheritance

```cpp
class ChildClass : access_specifier ParentClass
```

Example:

```cpp
class Dog : public Animal
```

Here:

- `Dog` → Child class  
- `Animal` → Parent class  
- `public` → Access specifier  

---

## Why Do We Use Inheritance?

### 1. Code Reusability
We don't need to write the same code again.

### 2. Better Code Organization
It helps represent **real-world relationships**.

### 3. Easier Maintenance
Changes in the parent class automatically reflect in child classes.

---

## Types of Inheritance

### 1. Single Inheritance

One child inherits from one parent.

```
Animal → Dog
```

---

### 2. Multilevel Inheritance

A class inherits from a class which itself is inherited from another class.

```
Animal → Mammal → Dog
```

---

### 3. Multiple Inheritance

A class inherits from more than one parent.

```
Teacher
   \
    Person → Student
```

(C++ supports this.)

---

### 4. Hierarchical Inheritance

Multiple classes inherit from one parent class.

```
      Animal
     /  |  \
   Dog Cat Lion
```

---

### 5. Hybrid Inheritance

Combination of two or more inheritance types.

---

## Advantages of Inheritance

- Code reuse  
- Reduces duplication  
- Improves readability  
- Models real-world relationships  

---

## Disadvantages of Inheritance

- Tight coupling between classes  
- Changes in parent class may affect child classes  
- Deep inheritance hierarchies can become complex  

---

## Key Terms

| Term | Meaning |
|-----|------|
| Base Class | The parent class |
| Derived Class | The child class |
| Reusability | Using existing code |
| IS-A Relationship | Relationship between child and parent |

Example:

```
Dog IS-A Animal
```

---

## Summary

Inheritance allows a class to **reuse properties and methods of another class**, helping build **clean and maintainable object-oriented programs**.