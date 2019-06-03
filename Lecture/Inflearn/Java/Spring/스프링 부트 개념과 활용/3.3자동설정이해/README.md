## 자동 설정 이해

    @SpringBootApplication
    는
    @SpringBootConfiguration
    @ComponentScan
    @EnabelAutoConfiguration
    과 같다.

### 패키지 스코드 주의
#### @ComponentScan
- @Component 어노테이션이 붙어 있을 클래스를 빈으로 등록하다
- @Configuration, @Repository, @Service, @Controller @RestController

#### @EnabelAutoConfiguration
- @ComponentScan으로 빈을 등록 후에 추가적으로 빈을 등록 한다.
- spring-factories
  - org.springframework.boot.autoconfigure.EnabelAutoConfiguration
  - 에 키값으로 부터 클래스를 찾아서 빈으로 등록
  - 조건에 따라서 (@Conditional...)
