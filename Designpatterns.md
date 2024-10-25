#### Design Patterns 
A pattern refers to a solution that can be resued to a common problem that occurs in specific context within software design.
pattern helps in providing a blueprint which can be later adapted to fit various situations,help to stream line the development process and improve code quality


**Key characterstics**
+ Reusuable : They can be applied to different modules with in same project , reducing the need to solve their issues repeatedly.
+ Best practice: Developers can avoid common mistakes by using patterns to store proven best practices.
+ Communication: Developers can better communicate ideas using established patterns. When someone mentions a design pattern, the team can understand the solution.
+ Decoupling: Many patterns promote loose coupling between components, making systems easier to understand, maintain, and extend.

#### Types of patterns in Java 
***Creational Patterns*** : These patterns deal with object creation mechanisms,aiming to create objects in a manner suitable for the situation.when there are multiple classes or hirearchies, this pattern helps to manage the complexity of object creation.
+ Abstract Factory: Creates families of related objects without specifying their concrete classes.
+ Builder: Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
+ Factory Method: Defines an interface for creating an object, but lets subclasses alter the type of objects that will be created.
+ Prototype: Creates new objects by copying an existing object (the prototype) rather than creating new instances from scratch.
+ Singleton: Ensures a class has only one instance and provides a global point of access to that instance.

***Structural Patterns***: These patterns focus on how classes and objects are blended to form a large structure. they help simplify the design by identifying the simple ways to realize the relationship between entities.
+ Adapter: Allows incompatible interfaces to work together by converting one interface into another. Existing interface --->  adaptee ----> adapter 
+ Bridge: Separates an abstraction from its implementation so that the two can vary independently.
+ Composite: Composes objects into tree structures to represent part-whole hierarchies, allowing clients to treat individual objects and compositions uniformly.
+ Decorator: Adds new functionality to an object dynamically without altering its structure.
+ Facade: Provides a simplified interface to a complex subsystem, making it easier to use.
+ Flyweight: Reduces the cost of creating and manipulating a large number of similar objects by sharing common parts.
+ Proxy: Provides a surrogate or placeholder for another object to control access to it.

***Behavioural Patterns*** : These patterns are concerned with algorithms and the assignment of responsibilities between objects. They help define how objects communicate and interact with each other.
+ Command: Encapsulates a request as an object, thereby allowing for parameterization of clients with queues, requests, and operations.
+ Interpreter: Defines a representation for a language’s grammar and provides an interpreter to evaluate sentences in the language.
+ Observer: Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified.
+ Strategy: Defines a family of algorithms, encapsulates each one, and makes them interchangeable, allowing the algorithm to vary independently from clients that use it.
+ State: Allows an object to alter its behavior when its internal state changes, appearing to change its class.
+ Memento: Captures and externalizes an object’s internal state without violating encapsulation, allowing the object to be restored to that state later.
+ Visitor: Represents an operation to be performed on the elements of an object structure, allowing you to define a new operation without changing the classes of the elements on which it operates.

***Note: GENAI has been used to understand the patterns***