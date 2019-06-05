## 내정 웹 서버 응용
- Goal : 내장 웹서버에 변경 및 설정 방법에 대해서 알아 본다
- 내장 웹서버 변경하기

```xml
<properties>
	<servlet-api.version>3.1.0</servlet-api.version>
</properties>
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-web</artifactId>
	<exclusions>
		<!-- Exclude the Tomcat dependency -->
		<exclusion>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-tomcat</artifactId>
		</exclusion>
	</exclusions>
</dependency>
<!-- Use Jetty instead -->
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-jetty</artifactId>
</dependency>

```
- 웹 서버 사용하지 않기

    spring.main.web-application-type=none

- 서버포트 변경하기

    server.port = 7070
    - Ramdom port

    server.port = 0

- Discover the HTTP Port at Runtime

    You can access the port the server is running on from log output or from the ServletWebServerApplicationContext through its WebServer. The best way to get that and be sure that it has been initialized is to add a @Bean of type ApplicationListener<ServletWebServerInitializedEvent> and pull the container out of the event when it is published.

https://docs.spring.io/spring-boot/docs/current/reference/html/howto-embedded-web-servers.html
