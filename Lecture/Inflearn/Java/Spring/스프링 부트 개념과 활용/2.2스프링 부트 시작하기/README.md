## 스프링 부트 시작하기
- maven 프로젝트 생성
- pom.xml에 의존성 추가 하기
  - parent
  - web  (이것을 추가 했을때, external library들이 쭉쭉 올라옴)
  - build maven plugin
- application class 생성하기
  - @SpringBootApplication 어노테이션 붙이기
  - 일반 main()함수에서 SpringApplication.run() 추가
  - 일반 main()함수 실행하듯이 실행
  - **와우!!** 톰캣서버가 뜸 ㅋㅋ
  - 어떻게 해서 이것이 가능? 뒤에 강의에서 설명해준다고 함 (어노테이션과 run메써드 분석~)
- Maven package
  - jar 파일 생성됨
  - Java -jar target/**.jar 실행
  - 역시 웹서버 생성


  
