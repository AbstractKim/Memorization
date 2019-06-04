## 자동설정 만들기: Starter와 AutoConfigure
Starter와 AutoConfigure를 만들어 봄으로써 실제로 스프링에서 사용되고 있는 원리를 이해한다.

1. 프로젝트 새로 생성 (autoconfigure를 제공할)
2. autoconfigure관련 의존성 추가
3. @Configuration 및 빈 설정
4. spring.factories파일 만들고 자동설정 파일 추가
5. mvn install (로컬 mvn저장소에 저장)

#### 문제점1. 덮어쓰기
어플에 새로운 빈을 등록하더라도 이전값이 적용. 왜? 새로운 빈은 @ComponentScan으로 등록이 되나, @EnabelAutoConfiguration에 에 의해서 이전 빈으로 다시 등록

###### 해결책
@Conditional...

#### 문제점2. 새로 빈등록하지말고 프라퍼티를 이용해서 값만 바꾸고 싶다
