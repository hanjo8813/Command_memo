# < Django >

<br>

## ⚙️ 명령어

### 장고 버전 보기
```
> python -m django --version
```

### 프젝 생성
```
> django-admin startproject '프젝이름'
```

### 앱 생성
```
생성 후 -> settings.py -> INSTALLED_APPS 파트에 앱 이름 추가.
> python manage.py startapp '앱이름'
```

### 서버 실행
```
> python manage.py runserver
```

### DB 테이블 모델링
```
> python manage.py inspectdb
```

### (배포용) static 파일 모아서 생성
```
> python manage.py collectstatic
```


<br>

## 참고 사이트

### 