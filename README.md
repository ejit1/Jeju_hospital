# 제주도 병원 찾기 및 후기 서비스
<br>

## 1. 목표와 기능

<br>

### 1.1 목표
- 지역 병원을 모아볼 수 있는 웹 서비스
- 해당 진료과목의 병원을 모아볼 수 있는 웹 서비스
- 영업을 하지 않는 병원은 노출이 되지 않아 혼선을 줄여주는 웹 서비스
- 해당 병원의 정보와 전반적인 후기를 모아보는 웹 서비스
  <br>

### 1.2 기능
- 제주데이터허브 "[보건, 복지] 병,의원 정보" 사용 (https://www.jejudatahub.net/data/view/data/859)
- 제주 지역과 진료과목에 따라 구분된 병원 목록 제공
  (서비스 제공 지역만 버튼 활성화)
- 병원의 만족도를 확인할 수 있는 별점 제공
- kakao map api 사용
- 로그인, 회원가입
- 후기 작성
  <br>
  <br>

## 2. 개발 환경 및 배포 URL
<br>

### 2.1 개발 환경

- Tools
    - Visual Studio Code, GitHub, Figma, ERD Cloud, Discord

<br>

**Back-End**

- Web Framework
    - Django 3.2 (Python 3.6.8)
- 서비스 배포 환경
    - AWS Lightsail
      - CentOS 7

<br>

**Front-End**

- Web
    - HTML5, CSS, JavaScript
- API
    - Bootstrap5, Kakao Map

<br>

### 2.2 배포 URL

- http://jejuhospital.oreum.icu/
  <br>
  <br>

## 3. 프로젝트 구조와 개발 일정

<br>

```bash
  └─ hackathon
      └─ main
          └─ migrations
          └─ static
          └─ templates
          |  admin.py
          |  apps.py
          |  models.py
          |  tests.py
          |  views.py
      └─ media
      └─ myvenv(가상환경)
      └─ tutorialdjango
          |  asgi.py
          |  settings.py
          |  urls.py
          |  wsgi.py
      │  db.sqlite3
      |  manage.py 
```

<br>

### 3.1 개발 일정 (WBS)

기간 : 2022년 08월 29일 ~ 2022년 09월 02일

<br>

<br>

## 4. 역할 분담
<br>

- FE : 김승우
- FE : 정혜연
- BE : 허현주
- BE : 오민영

<br>

<br>

## 5. UI / BM
<br>

**메인 화면**

<img style="width: 900px" align="left" src="C:\Users\Play\AppData\Roaming\Typora\typora-user-images\image-20230605183010946.png" alt="image-20230605183010946" />

- 반응형 웹페이지 : 창 사이즈에 따라 메뉴 구성 변화
  - header 메뉴바
  - content 진료과목 선택창
- 로그인, 회원가입 : 중복된 아이디, 비밀번호 입력 에러 등등 각 상태마다 alert 창 경고
  <br>

**병원목록 화면**

<img style="width: 900px" align="left" src="C:\Users\Play\AppData\Roaming\Typora\typora-user-images\image-20230605183042408.png" alt="image-20230605183042408" />

- 제주데이터허브 공공데이터 : 병원리스트 제공
- 공공데이터의 최신버전으로 정렬하여 불러온 데이터 값의 중복 방지
  <br>

**병원정보 및 리뷰 화면**

<img style="width: 900px" align="left" src="C:\Users\Play\AppData\Roaming\Typora\typora-user-images\image-20230605183624738.png" alt="image-20230605183624738" />

- 병원의 디테일 정보 : 병원 이름, 주소, kakao map api를 사용한 주소 마킹, 후기 모음
- 후기 : 로그인한 사람에 한해서 사용가능, 제목, 내용, 별점이 다 작성되어야 등록 가능

<br>

<br>

## 6. 데이터베이스 모델링(ERD)

<br>

<img style="width: 900px" align="left" src="https://user-images.githubusercontent.com/94173023/188053009-61351f80-5786-4afb-b72d-7e21c1d2256d.jpg" alt="ERwin" />

<br>
