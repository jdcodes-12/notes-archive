# Design Patterns | Overview 

## Terminology:
- `interface`: public part of an object, describe how to interact with it.
- `idioms`: most basic & low-level design patterns
- `architectural patterns`: high-level design patterns to structure ("architect") the program

## Object Oriented Programming
- Programming paradigm focused utilizing classes & objects
  - `class`: a blueprint of an object. Defines an objects structure.
  - `object`: something that contains data and behavior. Instace of a class.
  - `behavior`: the actions the "object" can do
  - `data`: describe the "object" (known as properties/fields)

- Classes
  - `parent class`: the main class some other class extends
  - `subclass`: a child class of a parent class (i.e. Dog extends Animal)
     - Animal = parent class
     - Dog = child class
  - `class heirarchy`: shows the relationship between classes 

- Subclasses
  - inherit data & behavior from their parent class
  - can "override" behavior of methods from parent class
    - may completely replace or enhance the default behavior

### Four Pillars of OOP
1. Abstraction: 
  - modeling of a real-world obejct or phenomemon
  - represents relevant details of the "object" to context of app beign built
  
2. Encapsulation:
  - `encapsulate`: to hide private details of a class from other objects
    - `private`: visible only inside the class itself
    - `protected`: visible in the current class & all subclasses of this class
    - `public`: visible to any code trying to access the current object

3. Inheritance
  - creating new classes from existing classes (i.e. code reuse)
  - subclasses have the same interface as their parent class
    - can't hide a method in a subclass if it's declared in the parent
    - must implement all abstract methods, even if not logicl to put in class
    - must implement all interfaces the parent class implements  
  - classes are often restricted to extending only one class

4. Polymorphism
  - ability to detect real class implementation when code is executed
    - enables the use of programming around interfaces & inheritance
    - polymorphism doesn't need to know the real type in the current context

  - objects "pretend" to be something else at runtime
    - then polymorphism tracks down the implementation of the "real" object 

#### Quick Note On Interfaces
- `interface`: publicly expose contract of an object
  - defines the behaviors (methods) that can be used on a certain object
  - concerned with abstraction & encapsulation
- classes can "implement" multiple intefaces at a time.

### Relations Between Objects

1. Dependency
  - weakest type of relation between classes
  - changes to one class might result in modifications to another class
  - occurs when using concrete class names in code
  - to reduce the coupling:
    - user interfaces or abstract classes instead of concerete implementations
  
2. Association
  - special kind of "dependency" relationship
    - an object always has access to the other objects it uses/interacts with.
    - permanent link between these artifacts

  - Object A interacts with or users Object B
    - can have bi-directional associate (where A uses B, and B uses A)

  - often used to associate an class field to some other object  

3. Aggregation
  - sepcial type of "association" representing various relationships between objects:
    - "one-to-many"
    - "many-to-many"
    - "whole-part"
  - an object usually "has" a set of other obejcts & acts as a container around these objects

4. Composition
  - kind of "aggregation"
  - one object is composed of 1+ instances of other objects.
    5- component can only exist as part of a container
  - strongest type

5. Implementation
  - Class A defines methods declared in interface B
  - Objects A can be treated as B
  - Class A depends on B

6. Inheritance
  - Class A inherits interface & implemenation of class B, but can extend it.
  - Objects A can be treated as B
  - Class A depends on B

## Design Patterns
- `design pattern`: 
  - typical solution to commonly occurring paterns in software design
  - like pre-made blueprints, which can be customized to solve a recurring problem in code
 
- Design patterns:
  - not code, rather high-level ideas on how to compose code to solve a problem
  - not an algorithm
  - abstractions on how to structure code; same pattern can be implemented in diff ways based on the project
  - vary in complexity & diffculty to implement
  
- A design pattern consist of:
  1. Intent: describes the problem & the solution
  2. Motivation: further epxlains the problem & the solution the pattern makes possible.
  3. Structure: classes represent each part of the pattern & how they are related
  4. Implementation: actually writing the pattern (varying based on language) into the code base. 

- Categories of design patterns:
  1. Creational: object creation mechanism; increasing code flexibility and reusability
  2. Structural: how to assembly classes & objects into larger structures, with flexibility & efficiency
  3. Behavioral: effective communcation & delegating responsibilites between objects

- Why learn patterns:
  - increase problem-solving by exposing starting points (the patterns themselves) to be proven to work
  - common language a development team can use to reason about the code.

## Software Design Principles

### Features of Good Design
1. Code Reuse

2. Extensibility

### Design Principles
1. Encapsulation what varies
2. Program to an Interface, not an Implementation
3. Favor composition over inheritance

### SOLID Design Principles
1. Single Responsibility Principle

2. Open/Closed Principle

3. Liskov Subsitution Principle

4. Interface Segregation Principle

5. Dependancy Inversion Principle 
