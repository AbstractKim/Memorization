## The Singleton Pattern
# One of Kind objects

Singleton Pattern은 static global access와 달리 우리가 원할 때 생성하고 없앨 수 있다. **Scope조절 가능**. 즉 resource낭비를 줄일 수 있다.

#### How to make Singleton?
- Make constructor as private
- create a method only one instance created and return
  - It will create only one instance or return an instance already created

**The Singleton Pattern** ensures a class has only one instance, and provides a global point of access to it.

#### Thread Issues
- Just add a keyword of 'synchronized' on getInstance()
- But 'synchronized' is expensive
  - Option 1. Do nothing if the performance of getInstance() isn't critical to your application
  - Option 2. Move to an eagerly created instance rather than lazily created one
  - Option 3. Use "Double-checked locking" to reduce the use of synchronization in getInstnace()


  #### 단점
  상속 불가


  [참고: Effective Java 3rd. item 3. enforce the single property with a private constructor or an enum type](Book\Java\Common\Effective Java 3rd\item3.enforce-the-singleton-property.md)
