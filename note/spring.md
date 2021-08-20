# Spring

<br>

## Annotation
> 어노테이션 종류 정리

### @Configuration

### @Bean

### @ComponentScan

```java
// 패키지 지정 방식
@ComponentScan(basePackages = {"패키지", ...})
// 클래스 지정 방식
@ComponentScan(basePackageClasses = {클래스명.class, ...})
```

### @Component

```java
@Service
@Repository
...
```

### @PropertySource

### @Value