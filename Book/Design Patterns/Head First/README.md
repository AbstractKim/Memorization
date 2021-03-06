# Head First - Design Patterns
우리는 왜 Design Pattern(이하 DP)을 공부해야 하는가? DP는 수 많은 선배 Engineer가 시행착오를 거쳐서 만든 경험의 집합체이다. 따라서, DP를 공부하고 적용하면 좋은 프로젝트를 만드는데 **시행착오를 줄일 수 있다**.

또한, DP를 배워야 하는 가장 중요한 이유는 **효율적인 소통방법**이다. 팀원간에 Design Structure에 대해서 이야기 할때, DP의 용어들로 이야기를 하면 서로간에 바로 이해할 수 있기때문에 소통의 비용을 줄일 수 있다.

DP를 통해서 라이브러리 또는 프래임워크를 (ex. JAVA LIB, SPRING 등) 조금 더 잘 이해할 수 있다. 물론 DP는 beyond language 이다.

Current: 4장 Baking with OO goodness: the Factory Pattern (Re 2)

SKIMMING 1, REPETITION 0.25

DESIGN PATTERN|JAVA|HEAD FIRST|ERIC FREEMAN|ELISABETH FREEMAN|  

[Head First - Design Patterns 책 링크](https://www.amazon.com/Head-First-Design-Patterns-Brain-Friendly/dp/0596007124)

## OO Principle
- Identify the aspects of your application that vary and separate them from what stays the same
- Take the part that vary and encapsulate them, so that later you can alter or extend the parts vary without those that don't
- Program to an interface, not an implementation
- Favor composition over inheritance
- Strive for loosely coupled designs between objects that interact
- Class should open for extension, but closed for modification
- **Dependency Inversion Principle:** Depend upon abstractions. Do not depend upon concrete classes.

## Design Pattern
- **Strategy pattern** defines a family of algorithms, encapsulates each one, and make them interchangeable. Strategy lets the algorithm vary independently from clients that use it
- **Observer pattern** defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and update automatically.
- **Decorator pattern** attach additional responsibilities to an object dynamically. Decorators provide a flexible alternative to subclassing for extending functionality.
- **The factory Method Pattern** defines an interface for created an object, but let subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses.
- **The Abstract Factory Pattern** provides an interface for creating families of related or dependent objects without specifying their concrete classes.
- **The Singleton Pattern** ensures a class has only one instance, and provides a global point of access to it.
