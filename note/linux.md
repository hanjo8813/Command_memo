# < Linux >

<br>

## ⚙️ 기본 명령어

### 열린 포트 확인
```sh
> netstat -tnlp
```

### 수정 권한 부여
```sh
> sudo chmod -R 777 [파일or디렉토리]
```

### 패키지 업데이트
```sh
> sudo apt-get update
> sudo apt-get dist-upgrade
```

### TimeZone 설정
```sh
# 서버 시간 보기
> date
# 서버 timezone 보기
> cat /etc/timezone
# timezone 설정하기
> sudo dpkg-reconfigure tzdata
```

<br>

## ⚙️ 설치 명령어

### Python 설치
```sh
> sudo apt update
> sudo apt-get install python-dev python3-dev
> sudo apt install python3-pip
```

### node.js 설치
```sh
> sudo apt-get install curl
> curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
> sudo bash nodesource_setup.sh 
> sudo apt-get install nodejs
> sudo apt-get install build-essential
```

### Docker 설치
```sh
> sudo apt update
> sudo apt install apt-transport-https
> sudo apt install ca-certificates
> sudo apt install curl
> sudo apt install software-properties-common
> curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
> sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
> sudo apt update
> apt-cache policy docker-ce
> sudo apt install docker-ce
```

### nginx 설치
```sh
> sudo apt-get install nginx
```

<br>

## 참고 사이트

### node.js 설치
- https://velog.io/@ywoosang/Node.js-%EC%84%A4%EC%B9%98

### nginx PID 오류 발생시
- https://blog.seabow.pe.kr/?p=8295

### Docker 설치
- [링크](https://velog.io/@wimes/AWS-EC2%EC%97%90-Docker-%EC%84%A4%EC%B9%98-%EB%B0%8F-Dockerfile%EB%A1%9C-%EC%9B%B9%EC%84%9C%EB%B2%84-%EA%B5%AC%EB%8F%99%EC%8B%9C%ED%82%A4%EA%B8%B0)