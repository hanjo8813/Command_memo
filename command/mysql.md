# < MySQL >

<br>

## DDL 기본문법

### CREATE

```sql
CREATE TABLE 테이블명(
  필드명 타입 NOT NULL AUTO_INCREMENT DEFAULT 값,
  ...
  PRIMARY KEY(필드명),
  FOREIGN KEY(필드명) REFERENCES 테이블명(필드명),
  INDEX 인덱스명(필드명)
);
```

### DROP TABLE
```sql
DROP TABLE [IF 조건] 테이블명;
```

### ALTER (ADD/ALTER)

```sql
ALTER TABLE 테이블명
[ADD/ALTER] 필드명 타입 옵션...;
```

### ALTER(DROP COLUMN)

```sql
ALTER TABLE 테이블명
DROP COLUMN 필드명 [CASCADE];
```

<br>

## DML 기본문법

### SELECT

```sql
SELECT [DISTINCT] 필드명
FROM 테이블명
JOIN 필드명 ON 기준설정(키값매핑)
WHERE 조건
GROUP BY 필드명1, 필드명2
ORDER BY 필드명 [ASC|DESC]
LIMIT N ;
```

### INSERT INTO

```sql
INSERT INTO 테이블명(필드명, ...)
VALUES (데이터, ...);
```

### DELETE

```sql
DELETE FROM 테이블명
WHERE 조건;
```

### UPDATE

```sql
UPDATE 테이블명
SET 필드명 = 데이터,
    ...
WHERE 조건;
```

<br>

## ⚙️ 명령어

### 외부 DB 접속
```
> mysql -u root -p --host '호스트 IP'
```

### DB 덤프파일(sql) export 
```
# sql 파일을 export로 원하는 위치에서 터미널을 연 후 명령어 실행
> mysqldump -u root -p 'DB 이름' > 'DB 이름'.sql
```

### DB 덤프파일(sql) import 
```
# 1. 빈 DB(스키마) 생성
> create database 'DB 이름'
> quit

# 2. import할 sql 파일을 원하는 위치로 이동 후 해당 위치에서 터미널 실행
# 3. import 명령어 실행
> mysql -u root -p '생성한 DB 이름' < 'sql파일 이름'.sql
```

### MySQL(ver 5.x) 비밀번호 변경
```
# mysql 내부에서 실행
> use mysql;
> select host, user, authentication from user;
> update user set authentication_string=password('비번') where user='유저이름';
> flush privileges;
```

<br>

## 참고 사이트

### 