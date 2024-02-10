# Django에서 DRF 개발을 위한 세팅 (w/ JWT)

## 1. 필요한 모듈 설치

다음과 같은 패키지가 필요

```python
djangorestframework # RESTful API 개발
dj-rest-auth # 인증 및 사용자 관리 구현(로그인, 로그아웃, 회원가입 및 소셜 로그인)
django-allauth # 다양한 인증 및 회원가입 옵션을 제공 (사용자 인증, 회원가입, 비밀번호 재설정 및 소셜 로그인)
djangorestframework-simplejwt # JSON Web Token (JWT) 인증을 구현
```

<br>

requirements.txt에 다음을 넣고 `pip install -r requirements.txt`로 설치한다.

```
asgiref==3.7.2
certifi==2023.7.22
cffi==1.16.0
charset-normalizer==3.3.2
cryptography==41.0.5
defusedxml==0.7.1
dj-rest-auth==2.2.4
Django==4.0.3
django-allauth==0.50.0
djangorestframework==3.13.1
djangorestframework-simplejwt==5.1.0
idna==3.4
oauthlib==3.2.2
pycparser==2.21
PyJWT==2.8.0
python3-openid==3.2.0
pytz==2023.3.post1
requests==2.31.0
requests-oauthlib==1.3.1
sqlparse==0.4.4
typing_extensions==4.8.0
tzdata==2023.3
urllib3==2.0.7
```

## 2. settings.py 설정

```python

# 앱 추가
INSTALLED_APPS = [
  ...,
  # DRF , JWT , 인증 관련 앱 추가
  'rest_framework',
  'rest_framework.authtoken',
  'dj_rest_auth',
  'django.contrib.sites',
  'allauth',
  'allauth.account',
  'allauth.socialaccount',
  'dj_rest_auth.registration',
  ...
]
```
