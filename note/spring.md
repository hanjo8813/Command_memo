# Spring

<br>

## Basic Annotation
> 설정관련 어노테이션 종류 정리

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

### @Autowired

### @ConfigurationProperties

```java
// 프로퍼티 파일 계층을 입력하면 하위 데이터를 긁어온다
@ConfigurationProperties(prefix = "카테고리")
```

### @Profile

```java
// 컴포넌트 파일에 달아줌
@Profile("프로필명")
// 여러개 지정 가능
@Profile( {"프로필명", ... } )
```

### @PropertySource

```java
// properties provider 클래스 만들때 사용
@PropertySource("프로퍼티명.properties")
```

### @Value

```java
// 시스템 환경변수도 가져올 수 있음
@Value("${프로퍼티 키값}")
@Value("${키값 : 없을때넣을값}")
```

### @ActiveProfiles


<br>

## HTTP Annotation
> API관련 어노테이션 종류 정리

### @RequestMapping

```java
@RequestMapping
@GetMapping
@PostMapping
@DeleteMapping
```

### @RequestParam

### @RequestBody

### @PathVariable



<br>

## Test Annotation
> 테스트 어노테이션 종류 정리

### @Test

### @DisplayName

### @Disabled

### @TestMethodOrder

### @Order

### @TestInstance

### @SpringBootTest

### @Before @BeforeAll @After @AfterAll

<br>

## Lombok Annotation
> Lombok 어노테이션 종류 정리

### @Slf4j