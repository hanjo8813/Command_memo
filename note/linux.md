# Linux

<br>

## ⚙️ 기본 명령어

### Linux

- `man` : 명령어 설명 보기
- `pwd` : 현재 디렉토리 위치 보기
- `ls` : 현재 디렉토리 안의 파일 보기
    - `ls -l` : 파일 상세정보까지 보기
    - `ls -a` : 숨어있는 파일까지 보기
    - `ls -t` : 파일을 최신순으로 보기
    - `ls -rt` : 파일을 오래된순으로 보기
- `cd` : 디렉토리 이동
    - `cd /` : root 디렉토리로 이동
    - `cd ~` : home 디렉토리로 이동 
    - `cd -` : 이전 디렉토리로 이동 
- `find [path] 옵션 정규식/표현` : 경로 하위에서 무언가 찾기
    - 옵션 `-type f` : 파일 찾기
    - 옵션 `-type d` : 디렉토리 찾기
- `which 명령어` : 특정 명령어의 위치를 찾아줌
- `touch 파일명` : 용량이 0인 파일을 생성 or 날짜 변경
- `cat 파일명` 파일의 내용 보기
- `echo $PATH` : 텍스트보기 (환경변수 볼때 사용)
- `mkdir 디렉토리명` : 디렉토리 만들기
- `cp A B` : A 파일을 B로 복사하기
- `mv A B` : A 파일을 B로 이동시킴
- `rm 파일명` : 파일 삭제
- `grep 문자열 파일명` : 파일이나 어떤 결과에서 해당 문자열을 찾아서 출력
- `env` : 현재 설정된 환경변수 보기
- `export` : 환경 변수를 지정, 변경하거나 현재 정의되어 있는 환경 변수를 보여주는 명령어 
- `df` : 현재 남은 디스크 공간 보기
- `ps` : 현재 실행중인 프로세스 보기
- `kill` : 멈춘 프로세스를 중지
- `tail` : 파일에서 마지막 10줄을 보여준다
- `chmod 권한 파일` : 파일의 권한 변경([참고](https://recipes4dev.tistory.com/175))
- `chown 유저 파일` : 파일의 소유자 변경 ([참고](http://www.redcrow.co.kr/wordpress/?p=532))

### vim

- `vi 파일명` : 파일을 생성 or 수정
- `i`, `a` : 입력모드 변경
- `esc` : 명령모드 변경
    - `^` : 행의 맨 왼쪽으로 이동
    - `$` : 행의 맨 오른쪽으로 이동
    - `H` : 화면 맨 위로 이동
    - `L` : 화면 맨 아래로 이동
    - `숫자G` : 해당 라인으로 이동
    - `dd` : 해당 라인 삭제
    - `x` : 문자하나 삭제
- `:q` : 저장 안하고 나가기
- `:wq` : 저장하고 나가기

<br>

## ⚙️ 자주 쓰는 명령어

### 포트 조작
```sh
# 열린 포트 확인
netstat -tnlp
# 포트를 사용하는 프로세스 확인
sudo lsof -i TCP:"포트번호"
# 포트를 사용하는 프로세스 종료
sudo fuser -k -n tcp "포트번호"
```

### 수정 권한 부여
```sh
sudo chmod -R 777 [파일or디렉토리]
```

### 패키지 업데이트
```sh
sudo apt-get update
sudo apt-get dist-upgrade
```

### TimeZone 설정
```sh
# 서버 시간 보기
date
# 서버 timezone 보기
cat /etc/timezone
# timezone 설정하기
sudo dpkg-reconfigure tzdata
```

<br>

## ⚙️ nginx 명령어

### 시작
```sh
sudo nginx
```

### 종료
```sh
sudo nginx -s stop
```

### 재시작
```sh
sudo nginx -s reload
sudo systemctl restart nginx
```

### 상태보기
```sh
sudo systemctl status nginx
```

<br>

## ⚙️ certbot 명령어

### 발급받은 인증서 확인
```sh
sudo certbot certificates
```

### 재발급 가능 여부 검사
```sh
sudo certbot renew --dry-run
```

### 재발급
```sh
sudo certbot renew
```

<br>

## ⚙️ 설치 명령어

### nginx 설치
```sh
sudo apt-get install nginx
```

### Java 설치 
```sh
sudo apt install openjdk-"버전"-jdk
```


### Python 설치
```sh
sudo apt update
sudo apt-get install python-dev python3-dev
sudo apt install python3-pip
```

### node.js 설치
```sh
sudo apt-get install curl
curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh 
sudo apt-get install nodejs
sudo apt-get install build-essential
```

### Docker 설치
```sh
sudo yum install docker
sudo systemctl start docker
```

```sh
sudo apt update
sudo apt install apt-transport-https
sudo apt install ca-certificates
sudo apt install curl
sudo apt install software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
sudo apt update
apt-cache policy docker-ce
sudo apt install docker-ce
```



<br>

## 참고 사이트

### node.js 설치
- https://velog.io/@ywoosang/Node.js-%EC%84%A4%EC%B9%98

### nginx PID 오류 발생시
- https://blog.seabow.pe.kr/?p=8295

### Docker 설치
- [링크](https://velog.io/@wimes/AWS-EC2%EC%97%90-Docker-%EC%84%A4%EC%B9%98-%EB%B0%8F-Dockerfile%EB%A1%9C-%EC%9B%B9%EC%84%9C%EB%B2%84-%EA%B5%AC%EB%8F%99%EC%8B%9C%ED%82%A4%EA%B8%B0)