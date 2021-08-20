# Django

<br>

## ⚙️ 명령어

### 장고 버전 보기
```sh
> python -m django --version
```

### 프젝 생성
```sh
> django-admin startproject '프젝이름'
```

### 앱 생성
```sh
생성 후 -> settings.py -> INSTALLED_APPS 파트에 앱 이름 추가.
> python manage.py startapp '앱이름'
```

### 서버 실행
```sh
> python manage.py runserver
```

### DB 테이블 모델링
```sh
> python manage.py inspectdb
```

### (배포용) static 파일 모아서 생성
```sh
> python manage.py collectstatic
```

### Django crontab 사용
```sh
# django-crontab 라이브러리 설치 필수
# 반드시 Django 세팅파일에 크론탭 등록 후 사용
> python manage.py crontab show
> python manage.py crontab add
> python manage.py crontab remove
```


<br>

## 참고 사이트

### 