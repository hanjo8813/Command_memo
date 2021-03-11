# < Git Memo >
### Git 명령어와 다양한 참고 사이트를 메모하는 repo입니다.

<br>

## ⚙️ 명령어

### Pull 하기
```
> git pull origin [브랜치]
```

### Clone 하기
```
> git clone [저장소 주소]
```

### remote 확인하기
```
> git remote -v
```

### config 확인하기
```
> git config --list
```

### 현 상태 확인하기
```
> git status
```

### 커밋 목록 확인하기
```
> git log
```

### config 설정
```
이름 설정 : > git config --global user.name '이름'
Email 설정 : > git config --global user.email '이메일'
```

### Stage로 add 하기
```
파일을 지정해서 add : > git add '파일명'
모든 변동 파일 add : > git add --all , git add *
```

### commit 하기
```
> git commit -m '메시지'
커밋 메시지 수정 : > git commit --amend
```

### add 취소하기 (Unstaged로 변경)
```
> git reset HEAD
```

### commit 취소하기
```
> git reset --hard HEAD^
```


<br>

## 참고 사이트

### Git 아이콘
- https://shields.io/

### 이모티콘 사용
- https://wepplication.github.io/tools/charMap/#emoji
- https://www.emojicopy.com/
- https://favicon.io/emoji-favicons/

### git LFS 사용법
- https://hwiyong.tistory.com/318




