# Object Oriented Programming | Design Patterns Overview

## Design Patterns

- design pattern:
  - typical solutions to commonly ocurring problems in software design
  - like customizable "blue-prints" to serve as a basis for solving problems
  - patterns:
    - are high-level concepts (abstractions) to use to follow code
    - can be used even outside an Object-Oriented paradigm
    - are not specific pieces of code (no copy & paste) 
    - are not algorithms (rather a high-level description, not low-level step)
    - can be applied to different programs in various ways
      - A banking program's Facade pattern may be implemented differently
        than a student management system's Facade pattern.
    - should not be used aimlessly; rather, use when it makes sense
    - usually are formally documented, so can look up and follow later
    - vary in complexlity, level of detail, and applicability to a system

- a pattern's documentation normally consists of:
  1. intent: describes the software design problem & pattern solution
  2. motivation: more on why the pattern makes solution possible
  3. structure: show each part of the pattern & how they are related
  4. code example: to help grasp the idea behind the pattern
 
- other things found in pattern documentation:
  1. appliciblity of the pattern
  2. implementatin steps
  3. relation to other design patterns

- types of patterns:
  1. idiomatic
    - low-level & most basic
    - applies to usually only a single programming language

  2. architectural patterns
    - high-level concepts & can be more complex
    - can be implemented in various programming languages
    - used to design architecture of an entire application

- why learn patterns:
  1. battle-tested solutions to common software design problems
     - increase problem-solving ability using OOP 
  2. define common language among the team 
     - team can be on same page
     - can be easier to reason about software as a team

## Categories of Design Patterns?
> Examples of the patterns can be found in the 
> `design-patterns` directory located in this
> current directory.

1. Creational: 
  - concerned with how objects are created in an application
  - aims to increase code reuse & flexibility of the codebase
  - patterns in category:
    1. factory method
    2. abstract factory
    3. builder
    4. prototype
    5. singleton

2. Structural:
  - explains how to assmble objects and classes into larger structures
  - focuses on keeping the structures flexible & efficient
  - patterns in category:
    1. adapter
    2. bridge
    3. composite
    4. decorator
    5. facade
    6. flyweight
    7. proxy
    
3. Behaviorial
  - concerned with how objects communicate with each other in a program
  - algorithms & responsibilities are delgated between objects  
  - pattern in category:
    1. chain of responsibility
    2. command
    3. iterator
    4. mediator
    5. memento
    6. observer
    7. state
    8. strategy
    9. template method
    10. visitor


