# 사전 준비

```
eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka
  instance:
    prefer-ip-address: true
```
위의 코드를 application.yml 파일에 추가한다. <br/>
들여쓰기 주의! server와 같은 라인으로 들어가야함 <br/>
<br/>
<br/>
```
implementation 'org.springframework.cloud:spring-cloud-starter-netflix-eureka-client'
```
build.gradle에 위의 의존성을 추가한다.
<br/>
<br/>
```
@EnableDiscoveryClient
```
위 어노테이션을 서비스의 mainClass 위에 추가한다
<br/>
```
dependencyManagement {
	imports {
		mavenBom "org.springframework.cloud:spring-cloud-dependencies:2022.0.3"
	}
}
```
만약 어노테이션 추가가 되지 않는다면 build.gradle에 위 코드를 추가한다. (모르겠으면 이현숙 부르기)

만약 application.yml과 application.properties가 둘 다 있다면 둘 모두에 application name을 정의해주어야한다. (그냥 application.properties를 지우는게 좋을듯)

그러면 이제 사전 준비 끝!


~~## 실행법~~
~~1. 이 프로젝트를 클론한다. (아무데나 해도 됨)~~
~~2. Discovery의 Eureka 실행~~
~~3. 각자 서비스 실행~~
~~4. Discovery의 Gateway 실행~~

~~**(http://localhost:8761) 에 자기 서비스 이름 올라가있나 확인**~~

# docker compose up 하면 알아서 됩니다~



<hr/>

# 안 되면 이현숙 부르기
