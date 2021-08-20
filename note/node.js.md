# < Node.js >

<br>

## ⚙️ 기본 명령어
> 패키지가 있는 폴더에서 터미널 실행

### js 파일 실행
```
> node '파일명'
```

### package.json을 참조하여 모듈 설치
```
> npm install
```

### 특정 모듈 설치
```
> npm install '옵션' '모듈명'
```

|옵션|설명|
|---|---|
|생략|명령어 실행한 폴더에 저장(node_modules/package.json)|
|-g|내 로컬에 글로벌로 설치|

<br>

## ⚙️ express 명령어

### package.json 참조하여 node.js 실행
```sh
> npm start
```

### nodemon으로 서버 실행
```sh
> nodemon 'config 시작 파일'
```

### sequelize-auto로 장고처럼 inspectdb 하기!
```sh
> sequelize-auto -o '디렉토리경로' -d 'DB명' -h '호스트 IP' -u 'user명' -p 3306 -x '비번' -e 'DB종류'
```

<br>

## ⚙️ Vue.js 명령어

### 서버 시작하기
```sh
> npm run serve
```

### 빌드하기
```sh
> npm run build
```


<br>

## 참고 사이트

### node.js 기본 실습
- https://victorydntmd.tistory.com/24

### sequelize-auto 
- https://www.hanumoka.net/2018/11/23/node-20181123-express-setting-sequelize/