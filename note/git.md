# Git 

<br>

## ⚙️ 명령어

### Pull 하기
```sh
> git pull origin [브랜치]
```

### Clone 하기
```sh
> git clone [저장소 주소]
```

### remote 확인하기
```sh
> git remote -v
```

### config 확인하기
```sh
> git config --list
```

### 현 상태 확인하기
```sh
> git status
```

### 커밋 목록 확인하기
```sh
> git log
```

### config 설정
```sh
# 이름 설정
> git config --global user.name '이름'
# Email 설정
> git config --global user.email '이메일'
```

### Stage로 add 하기
```sh
# 파일을 지정해서 add
> git add '파일명'
# 모든 변동 파일 add
> git add --all , git add *
```

### commit 하기
```sh
> git commit -m '메시지'
# 커밋 메시지 수정
> git commit --amend
```

### add 취소하기 (Unstaged로 변경)
```sh
> git reset HEAD
```

### commit 취소하기
```sh
> git reset --hard HEAD^
```

### 충돌무시 Pull
```sh
# pull 받는 저장소를 강제로 최신화 시킬때만 사용
> git fetch --all
> git reset --hard origin/master
> git pull origin master
```

### git 캐시 삭제
```sh
> git rm -r --cached .
> git add .
> git commit -m "어쩌구"
```

<br>

## 참고 사이트

### Git 아이콘
- https://shields.io/

### git LFS 사용법
- https://hwiyong.tistory.com/318

