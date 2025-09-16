

# INHERITANCE IN C++

**Aim:**
To study and implement different types of inheritance in C++.

**Tools Used:**
VS Code or Online C++ Compiler

---

## Theory

Inheritance is one of the core features of Object-Oriented Programming in C++. It allows a **derived class** to reuse data members and functions from a **base class**. This improves **code reusability**, reduces duplication, and makes programs more manageable.

---

### Types of Inheritance in C++

1. **Single Inheritance**

   * A derived class inherits from only one base class.
   * Simplest form of inheritance.
   * **Example:** `Car` inheriting from `Vehicle`.
   * **Use case:** When a new class is just an extension of one class.

2. **Multiple Inheritance**

   * A derived class inherits from more than one base class.
   * Helps combine features of different classes into one.
   * **Example:** `SmartCar` inheriting from both `Vehicle` and `Device`.
   * **Use case:** When a new class needs to represent multiple functionalities.
   

3. **Multilevel Inheritance**

   * A class is derived from another derived class (a chain of inheritance).
   * The last class inherits properties of both its parent and grandparent.
   * **Example:** `Dog → Mammal → Animal`.
   * **Use case:** When features are built step by step in levels.

4. **Hierarchical Inheritance**

   * Multiple derived classes inherit from a single base class.
   * **Example:** `Dog` and `Cat` both inherit from `Animal`.
   * **Use case:** When different subclasses share common features of one base.

5. **Hybrid Inheritance**

   * A combination of two or more inheritance types.
   * **Example:** Some classes using multiple inheritance while others follow hierarchical.
   * **Use case:** To model complex real-world systems.

---

### Effect of Access Specifiers in Inheritance

1. **Public Inheritance**

   * Base **public** → remains **public** in derived.
   * Base **protected** → remains **protected** in derived.
   * Base **private** → not accessible directly.
   * **Use case:** When the derived class is a true extension of the base.

2. **Protected Inheritance**

   * Base **public** and **protected** → become **protected** in derived.
   * Not accessible directly from outside the class.
   * **Use case:** To restrict base features from outside access, but allow inside derived.

3. **Private Inheritance**

   * Base **public** and **protected** → become **private** in derived.
   * Completely hidden from further derived classes.
   * **Use case:** When inheritance is used only for implementation, not for an “is-a” relationship.

4. **Private Members**

   * Base private members are **never inherited directly**.
   * They can only be accessed through base class public/protected methods.

---

## Algorithms

### 1) Access Specifiers in Inheritance

**Description:** Demonstrates how `public`, `protected`, and `private` members behave differently under public and protected inheritance.

**Algorithm:**

1. Create base class `Vehicle` with:

   * `private cost`,
   * `public brand, color(), showCost()`,
   * `protected displayInfo()`.
2. Create `car` (publicly inherits `Vehicle`) with model and `speed()` that calls `displayInfo()`.
3. Create `twowheeler` (protectedly inherits `Vehicle`) with type and `speed()`.
4. In `main()`, create objects of `Vehicle` and `car`, and call their methods.
5. Observe that `twowheeler.color()` is inaccessible from outside.
6. End.

**Key Learning:**

* Public inheritance keeps access unchanged.
* Protected inheritance restricts access.
* Private members remain hidden.

---

### 2) Single Inheritance

**Description:** Demonstrates simple inheritance of properties and functions from a single base class.

**Algorithm:**

1. Create base class `Vehicle` with brand and `color()`.
2. Create derived class `Car` with model and `speed()`.
3. In `main()`, create a `Car` object.
4. Call `color()`, access brand and model, and call `speed()`.
5. End.

**Key Learning:**
Derived classes can directly use public members of the base class.

---

### 3) Multiple Inheritance

**Description:** A derived class (`SmartCar`) inherits from two base classes (`Vehicle` and `Device`).

**Algorithm:**

1. Create base class `Vehicle` with `showType()`.
2. Create base class `Device` with `showName()`.
3. Create derived class `SmartCar` that inherits both and adds `showDetails()`.
4. In `main()`, create `SmartCar` and call `showDetails()`.
5. End.

**Key Learning:**
A derived class can combine the features of multiple base classes.

---

### 4) Multilevel Inheritance

**Description:** A chain of inheritance where each derived class extends another.

**Algorithm:**

1. Create base class `Animal` with `eat()` and `sleep()`.
2. Create class `Mammal` inheriting from `Animal` with `walk()`.
3. Create class `Dog` inheriting from `Mammal` with `bark()`.
4. In `main()`, create `Dog` and call all four functions.
5. End.

**Key Learning:**
Derived classes inherit features not just from their parent, but also from grandparents.

---

### 5) Hierarchical Inheritance (with multilevel extension)

**Description:** Demonstrates multiple classes inheriting from one base, and extending them further.

**Algorithm:**

1. Create base class `Animal` with `eat()`.
2. Create class `Dog` (inherits `Animal`) with `bark()`.
3. Create class `Cat` (inherits `Animal`) with `meow()`.
4. Create `WhiteCat` (inherits `Cat`) with `colour()`.
5. Create `BlackCat` (inherits `Cat`) with `colour()`.
6. In `main()`, create objects of all classes and call their methods.
7. End.

**Key Learning:**

* One base class can serve multiple derived classes.
* Derived classes can themselves be extended further.

---

## Key Learning Outcomes

* **Access Specifiers:** Control how members are inherited.
* **Single Inheritance:** Direct one-to-one inheritance.
* **Multiple Inheritance:** One class inherits from more than one base.
* **Multilevel Inheritance:** Classes inherit in a chain.
* **Hierarchical Inheritance:** One base → multiple derived.
* **Code Reuse:** Inheritance reduces redundancy and increases clarity.

---

## Applications

* **Games:** Base `Character` → `Player`, `Enemy`, `NPC`.
* **Banking Software:** Base `Account` → `SavingsAccount`, `CurrentAccount`.
* **Education System:** Base `Person` → `Student`, `Teacher`.
* **Vehicles:** Base `Vehicle` → `Car`, `Bike`, `Truck`.

---

## Advantages

* Promotes **code reusability**.
* Makes relationships clear (is-a relationship).
* Easier to extend existing code.
* Supports **polymorphism** and dynamic behavior.

