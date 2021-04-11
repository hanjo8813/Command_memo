# < MySQL Memo >
### MySQL 명령어와 참고 사이트 메모

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

<br>

## 참고 사이트

### 