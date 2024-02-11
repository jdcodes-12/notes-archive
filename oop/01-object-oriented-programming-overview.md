# Obejct Oriented Programming | Overview & Understanding

## What Is Object Oriented Programming?
> Quick note: In programming there are various "paradigms" 
> or ways of writing software programs. There is Procedural,
> Functional, and Object-Oriented (OOP) approaches. OOP is a 
> very common approach of writing modern, enterprise level 
> applications.
>
> But keep in mind, the paradigm used to write the software in
> question depends on the project's requirements and the limitations 
> and strengths of the underlying programming language. For example
> Golang (a.k.a GO) is not the best for OOP, where as Java is
> good for OOP, and something like Scala would be good for functional
> progrmaming.

### Object Oriented Programming Terminology
- `object-oriented programming`: programming paradigm that uses classes and objects
- `OOP`: alias for Object-oriented programming
- `class`: determines how an object will behave and what properties it will have (a "blueprint")
- `object`: a singular instance of a class type. Stored on heap memory.
- `instance`: a unique refernece of a object type in heap memory (compared by hash code & equals)
- `parent class`: the class type that provides methods and fields to a child class type
- `child class`: the class type that extends (inherits) a parent class type
- `super class`: another name for parent class
- `sub class`: another name for child class
- `interface`: abstract type that defines behaviors (methods) to implement. Does not produce obejcts.
- `abstract`: has no implementation details or cannot be used to create object instances
- `concrete`: actual implemtation of a class type. Products new objects.
- `abstract class`: abstract class type, often used for base type that should not produce obejcts

### Pillars of OOP
1. Abstraction
  - model of a "real-world" object (tangible or intangible), phenomenon, event, etc.
  - the model is scoped to a specific context
    - represents details of the underlying object w/ high accuracy per its current context

2. Encapsulation
  - hiding parts of an object's state & behavior from the rest of the program
  - determines method & field visibility of a class
  
3. Inheritance
  - enables building new class types (subclasses) via reusing parts of an existing class
  - primarly for code reuse throughout a program
  - most programming languages
    - allow class to only "extend" (e.g. inherit) one parent class
    - allow classes to *implement* multiple interfaces

4. Polymorphism
  - enables programs to detect the "real"/"concrete" implementation of objects during runtime
    - does this even if the real type is unknown within a given context (file, module, etc.)
    - objects "pretend" to be something else (usually a subclass or some interface)

  - useful in creating flexible software
    - reduces tight coupling of components (classes, interface, etc.)
    - can make programs easier to maintain 

## Relationship Between Objects

- Relationship Types
  1. Dependency
  2. Association
  3. Aggregation
  4. Composition
  5. Implementation
  6. Inheritance

- Dependency
  - most basic & weakest type of relation between calsses
  - occurs when changing one class can lead to modifications of another class type
  - often occurs when *concrete class names* are used, such as when:
    1. instantiating new objects (via constructor calls)
    2. specificying specific types in method signatures, etc.
  - use interface or abstract classes instead of concrete class types reduces the tight coupling

- Association
  - one object uses or interacts with another object
  - can have uni- or bi-directional association between objects
  - special kind of dependency where:
    - underlying object always has access to the objects it interacts with (like a permanent link)
  - occurs when:
    - a class field contains another external object type
    - a class method returns another external object type

- Aggregation
  - represents various degress of relationships between multiple objects:
    1. One-to-many
    2. Many-to-many
    3. Whole-part

  - the aggregate class:
    - contains a set of other objects (zero to many)
    - serves as a container or collection
    
  - the "aggregate" object:
    - can be part of multiple aggregate containers
    - works even when not linked to an aggregate container
  
  - Weaker than Composition, but stronger than simple Association

- Composition
  - a class type is made up of one or more other objects
  - the "composition" object, once instantiated, will have instances of various objects
  - components that make up the class, can only be functional (and should be intended) for that class
    - underlying components should not be able to exist by themselves without being wrapped by the
      "composition" class
  - strongest "Association" relationship

### Mindmap of Relationships
1. Dependency: 
  - Class A can be affected by direct/indirect changes in class B

2. Association: 
  - Object A knows about object B
  - Class A depends on B

3. Aggregation:
  - Object A knows about object B, and consists of B
  - Class A depends on (has a dependency with) class B 

4. Composition:
  - Object A knows about Object B, consists of B, and manage's B life cycle.
  - Class A depends on B.

5. Implementation:
  - Class A defines method declared in interface B.
  - Obejcts A can be treated as class B.
  - Class A depends on B

6. Inheritance
  - Class A inherits interface and implementation of Class B
  - Class A can extend Class B
  - Objects A can be treated as Object B
  - Class A depends on Class B
