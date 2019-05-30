## Dagger 2 0 A new Type of dependency injection

[링크](https://www.youtube.com/watch?v=oK_XtfXPkqw)


#### 순서
###### DI란 무엇인가?
왜??
###### SPRING DI
by XML 2년 전 이야기ㅎ
-  Solutions
  - initialization ordering
  - instance management (scoping)
- Issues
  - The XML is almost as verbose as the Java
  - Runtime validation of configuration
  - Runtime validation of the graph
  - Untraceable application flow
  - Map-like API

###### Guice
- New configuration options enabled by Java 1.5 language features
- Decreased and decentralized configuration
- Entirely written and executed in Java
- @Inject constructor
- bind and @Provides by extending AbstractModule
- What is the problem? (runtime error)
  - What happens if we forget a binding?
  - But worst of all, code becomes untraceable.
- Solutions
  - Binding discovery
  - Greatly reduced configuration
  - Configuration near configured code
  - Pure Java configuration
- Issues
  - Runtime validation of the graph
  - Untraceable application flow
  - Synthetic classes
  - Map-like API

###### Dagger 1
- Configuration API is basically the statically inspectable API from Guice
- Reduce features to streamline only to the safest, most effective featureset
- Move portions of the workload from runtime to compile time
  - Error reporting at complie time without special tooling
  - Efficient provision
- Take the reflection overhead out of provision
- what happens if we forget a binding?
  - we will get to know at compile time
- Solutions
  - Compile-time validation of portions of the graph
  - Easy debugging; entirely concrete call stack
  - Highly efficient provision
- Issues
  - Ugly generated code
  - Runtime graph composition
  - Inefficient graph creation
  - Partial traceability
  - Map-like API

###### Dagger 2
  Focus on the developer experience
  - Traceability
    - Navigate the entire application with "find usages" and "open declaration"
    - Trace through code that is clear and well-structured
  - Clarify the API
    - Simpler @Module declaration
    - No more "maps"
  -Performance
    - As fast as hand-written code
    - No coding around the framework

**the strategy**
- Keep (more-or-less) the Dagger API for configuration. It works.
- Generate simple Java at compile time for the entire stack that looks as close to hand-written DI code as possible
- Validate all framework/configuration preconditions at compile time
- Unify user-defined types with generated type through limited, well-defined entry points

[참고 AutoValue](https://github.com/google/auto/blob/master/value/userguide/index.md)

** The Implementation **
- The Standard DI API (JSR 330) declares exactly 1 interface
``` java
public interface Provider<T> {
  T get();
}
```

** @Component **

- Solutions
  - Compile-time validation of the entire graph
  - Easy debugging; entirely concrete call stack for provision and creation
  - Fully traceable
  - POJO API
  - Performance
- Issues
  - Less flexible
  - No dynamism
  - No automated migration path from Guice
