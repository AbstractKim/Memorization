## Item 3. Enforce the singleton property with a private constructor or an enum type
- 테스트 하기 힘들다
  - mock하기 힘들기 때문
  - 상위 interface로 부터 타입을 주는 구현이 없는 이상 힘들다

**보통 두 가지 방법으로 구현**
- **public static final 필드 멤버로 생성**
  - 간단하고 명백함
- **static factory method**
  - Flexibility: singleton이 아니게 쉽게 바꿀 수 있다고함. API의 변경 없이. 잘 모르겠음. 예가 있었으면 좀더 좋았을 것 같다
  - 'generic singleton factory'를 쓸수 있다고 하는데 _item 30_ 을 봐야할듯
  - method reference를 쓸 수 있다. 이건 이해;;ㅎ
- static factory method의 장점을 쓸일 없으면 그냥  public static final 필드 멤버로 생성해라
- Serializable (_Itme 12_)
  - 단순히 'Serializable'을 구현하는 것으로 안됨
  - 모든 필드를 'transient'로 선언하고 'readResolve' method를 제공해야함 (_Item 89_).
  - 이렇게 안하면, deserialize 할때 마다 새로운 인스턴스가 생성 된다고 함

**a single-element enum** 방법으로 생성
  - 간단하다고 함
  - 그래서, 종종 **best way** 라고
  - 하지만, enum이 아닌 다른 class를 상속해야 한다면 사용하지 말라



[참고 추천링크 by whiteship](https://www.oracle.com/technetwork/articles/java/javaserial-1536170.html)

[참고 HeadFirst- the singleton pattern](AbstractKim/Memorization/Book/Java/Design Patterns/Head First/Ch5the singleton pattern/ch5.the-singleton-pattern.md)
