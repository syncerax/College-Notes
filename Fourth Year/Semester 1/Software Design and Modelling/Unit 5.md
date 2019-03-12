# Software Design and Modelling

# Unit 5: Design Principles and Patterns

### Introduction to Patterns

- Experienced developers often build up a collection of general principles and idiomatic solutions that guide them in the creation of software. These principles are called patterns if they are codified in a structured format describing the problem and solution and given a name.
- In object oriented (OO) design, a pattern is a named description of a well known problem/solution pair that can be applied to new contexts.
- Ideally, a pattern provides advice on how to apply it in different circumstances and discusses its variations, implementations and tradeoffs.
- A design pattern essentially comprises of the following elements:
  - **Name** defines a design pattern's problem, solution and consequences.
  - **Problem** illustrates the situation in which the design pattern should be applied.
  - **Solution** is typically advice as to how the problem should be addressed. It is not a specific solution or implementation.
  - **Consequences** are the results and trade-offs of applying that design pattern.

### GRASP

- GRASP is an acronym for General Responsibility Assignment Software Patterns.
- It involves the strategies for assigning responsibilities to the classes and objects involved in OO software design.
- GRASP is a collection of 9 patterns: (LHCCIIPPP)
  - Low Coupling
  - High Cohesion
  - Creator
  - Controller
  - Information Expert
  - Indirection
  - Pure Fabrication
  - Protected Variations
  - Polymorphism
- All these patterns answer some problems that are common to almost every OO software development project.
- These techniques have not been created to invent new ways of working, but to document and standardise old, tried and tested principles in OO design.

### Creator

- **Problem:** Who should create an instance of class A?
- **Solution:** Assign the responsibility of creating an instance of class A to class B if one of the following is true (the more the better):
  - Instances of B "contain" or compositely aggregate instances of A.
  - Instances of B record instances of A.
  - Instances of B closely use instances of A.
  - Instances of B have the information required to create instances of A.

### Information Expert

- This principle is used to decide where to delegate responsibilites. These responsibilites include methods, computed fields, etc.
- **Problem:** What is a basic principle by which to assign responsibilites to objects.
- **Solution:** Assign a responsibility to the class that has the information needed to fulfill it.

### Low Coupling

- Coupling is a measure of how strongly one element is connected to, has knowledge of, or depends on other elements. When there is coupling or a dependency, if the depended-upon element changes, the dependant element may be affected.
- Low Coupling is an evaluative pattern, which means that it is used to evaluate existing designs. It describes how to assign responsibilites to support:
  - Low dependency between classes
  - Low impact, in a class, of changes in other classes
  - High reuse potential
- **Problem:** How to reduce the impact of change?
- **Solution:** Assign responsibilties so that unnecessary coupling remains low. Use this principle to evaluate alternatives.

### Controller

- A simple layered architecture contains a UI layer and a domain layer. UI objects should not contain application logic, such as calculating a player's move. They should pick up events (like a mouse click) and delegate the requests to objects in the somain layer.
- **Problem:** Which first object beyond the UI layer receives and co-ordinates or controls a system operation?
- **Solution:** Assign the responsibility to an object representing one of these choices:
  - Represents the overall "system", a "root object", a device that the software is running within, or a major subsystem.
  - Represents a use case scenario within which the system operation occurs.

### High Cohesion

- High Cohesion is an evaluative design pattern that attempts to keep objects appropriately focused, manageable and understandable.
- Cohesion informally measures how functionally related the operations of a software element are. If an element has high cohesion, it means that its responsibilities are strongly related and highly focused. Elements with low cohesion suffer from being hard to comprehend, reuse and maintain.
- High Cohesion is generally used in support of Low Coupling, since bad (low) cohesion goes hand in hand with bad (high) coupling.
- **Problem:** How to keep objects focused, understandable and manageable, and as a side effect, support Low Coupling?
- **Solution:** Assign responsibilities so that cohesion remains high. Use this pattern to evaluate alternatives.

### Polymorphism

- **Problem:** How to handle alternatives based on type? How to create pluggable software components?
- **Solution:** When related alternatives or behaviours vary by type (class), assign the responsibility of defining the variation of behaviours to the type for which the behaviour varies.

### Pure Fabrication

- **Problem:** What object should be assigned responsibility when you do not want to violate Low Coupling and High Cohesion (or other principles), but when solutions offered by Information Expert (for example) are not appropriate?
- **Solution:** Assign a highly cohesive set of responsibilities to an artifical convenience class that does not represent a problem domain concept, but is simply something made up (fabricated) to support high cohesion, low coupling and reuse, so the design is very clean (pure).

### Indirection

- This principle supports low coupling between two elements by assigning the responsibility of mediation between them to an intermediate class.
- **Problem:** Where to assign responsibility to avoid direct coupling between two or more elements? How to de-couple objects so that low coupling is maintained and reuse potential remains high?
- **Solution:** Assign the responsibility to an intermediate object to mediate between other components so that they are not directly coupled. The intermediary creates an indirection between the other components.

### Protected Variations

- This pattern protects elements from variations in other elements by wrapping the focus of instability with an interface.
- **Problem:** How to design objects, subsystems and systems so that variations or instabilities in these elements do not have an undesirable impact on other elements?
- **Solution:** Identify points of predicted variation or instability and assign responsibilities to create a stable interface around them.