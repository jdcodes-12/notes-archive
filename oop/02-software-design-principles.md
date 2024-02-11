# Object Oriented Programming | Software Design Principles

## Software Design Principles
> The following are principles that can help ensure quality
> object-oriented (OO) software applications.

### Principle 1: Encapsulate What Varies
- identify parts of the application that varies & separate those from parts
  that are commonly shared across application

- aims to reduce the effect of changes made to the codebase

- ecapsulation can happen on various levels:
  1. Method level
  2. Class level

### Principle 2: Program to an Interface, not an Implementation
- try to have dependencies to abstract classes or interfaces & not concrete
  class types

- aims to produce code flexibility. Making changes easier.

### Principle 3: Favor Composition Over Inheritance
- avoid deep class hiearchies/inheritance chains

- composition:
  - parent object controls the lifecyle of nested objects it contains
  - Object A is made up (composed of) object A, B, C, D, etc..
  

- inheritance can be good, but when overused it can make the codebase:
   1. tightly coupled
   2. extremely hard to change as the codebase grows

- problems that occur from relying on inheritance too much:
  1. subclass cannot reduce the interface of the superclass
    - must implement all abstract methods of teh parent class even if NOT
      to be used in the subclass (BOILERPLATE && UNUSED code)

  2. when overriding methods, need to make sure that the new behavior
     is compatible with the base one.
    - important because objects of the subclass may be passed to any 
      code that expects objects of the superclass. Can lead to passing bad
      or wrong functionality into a specific context

  3. inheritance breaks encapsulatino of superclass
    - internals of the superclass now expose to the subclass
    - vice-versa, when a programmer modifies a superclass to be aware of a
      subclass to make extensions (don't do this)

  4. superclasses are tightly coupled to subclasses
      - changing a superclass functionality may break subclass functionality

  5. reusing code via inherithance could lead to parallel inheritance hierarc
     chies.
    - can increase amount of code signigifcantl if the class hiearchy
      becomes too big horizontaly.



## SOLID Principles
> The following principles originated from Robert C. Martin.
> Discussed in his book **Agile Software Develpoment, Principles, 
> Patterns, and Practices**. They are intendted to help make 
> software designs more understandable, flexible, and maintainable.
>
> One *very important* to note, is that it can become very easy to
> over engineer an application/program if these principles are 
> applied aimlessly (without reason). Instead, before attempting
> to apply any of the following principles, analyze the softawre in
> question to see if the requirements justify trying apply a handful
> of these principles.
> 
> Striving to achieve these principles is good, but always be prag-
> matic and do not take these principles as dogma (absolute musts!).

1. (S)ingle Responsibility Principle
  - a class should have one reason to change
  - aim to encapsulate related functionality to specfic classes
  
2. (O)pen/Closed Principl
  - classes should be open for extension but closed for modification
  - a class is open when:
    - can extend it via a subclass & can override it's behavior
  - use to extend classes that are already in production
    - reduce risk of breaking the tested, reviewed, class in production

3. (L)iskov Substitution Principle
  - replacing parent class type with child class type should not break code
  - critical concept when developing libraries & frameworks
  - follows these rules:
    1. parameter types in a method of a subclass should match or be more
       abstract thatn parameter types in the method of the superclass

    2. return type in method of subclass should match or be a subtype of
       the return type in the method of the superclas.

    3. a method in a subclass shouldn't throw types of exceptions which
       the base method isn't expected to throw.
  
    4. a subclass should not strengthen pre-conditions
    
    5. a subclass should not weaken post-conditions

    6. invariants of a superclass must be preserved

    7. a subclass should not change values of private fields in the superclass

 
4. (I)nterface Segration Principle
  - classes should not be forced to depend on methods they do not use
    - make "narrow" interfaces which commonly shared logic
 
5. (D)ependency Inversion Principle
  - high-level classes should not depend on low-level classes.
    - both classes should depend on abstractions
    - abstractions should not depend on details
    - details should depend on abstractions

  - low level class:
    - impelment basic operations (connect to DB, work with network, etc.)
  
  - high-level class:
    - contain complex business logic & directs low-level classes to do somethi
      ng.
