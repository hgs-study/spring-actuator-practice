# spring-actuator-practice

+ 의존성 추가
```java
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-actuator'
}
```

+ http://localhost:8080/actuator

![image](https://user-images.githubusercontent.com/76584547/161757358-48bb0dad-62c1-43de-bb3f-26dd3e576121.png)


+ http://localhost:8080/actuator/health

![image](https://user-images.githubusercontent.com/76584547/161757560-15ed2a9f-936b-4d8c-bfd6-bcd0e0e8f3a1.png)

+ actuator + circuitbreaker
```
    https://resilience4j.readme.io/docs/getting-started-3
```

+ 모든 엔드포인트 사용
```java
application. yml

management:
  endpoints:
    web:
      exposure:
        include: "*"

```

+ 특정 엔드포인트만 허용
+ application.yml에 management.endpoints.enabled-by-default: false를 추가하면 모든 Actuator가 disable된다.
만약 특정 Actuator만 허용하고 싶다면 이렇게 할 수 있다
```java
managementendpoints.enabled-by-default: false
management.endpoints.info.enabled: true
management.endpoints.health.enabled: true
```
