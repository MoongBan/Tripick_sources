# _Tripick Main Page_


![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/7b7fd177-6fab-48c1-99c9-fbeb8d77d6e1)

---
## ✨ Description
```
기존 기차 예매 사이트 인터페이스의 불편함을 개선하고, 
놀거리와 먹거리 정보를 간편하게 Pick! 할 수 있는 사이트입니다. 
```


## 🔍 Overview
### 1.유저 회원가입 페이지
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/79a7fcfd-e27d-4b13-8e7b-8586cece7210)
JavaScript 사용하여 중복체크 구현

### 2. 놀거리, 먹거리 해시태그 기능
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/9d58926d-eca6-432c-bd79-7e1001e165bf)
키워드에 맞는 버튼을 클릭하면 각각의 버튼이 고유의 ThemeCode로 조립되어 적절한 정보 출력

### 3. 놀거리, 먹거리 상세정보 조회 페이지
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/aa1ab3c1-ef47-4386-bcaf-97134d18b8fa)
상세정보 페이지에서 저장(북마크), 리뷰작성, 예매하기(기차예매 연동), 리뷰(댓글) 기능 구현
"롯데월드 어드벤처블로그 글도 함께 읽어보세요" 버튼을 통해 블로그 글로 이동 가능. (홍보를 원하는 장소의 경우 블로그 글 작성 후 링크 가능)

### 4. 기차 예매 기능
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/c8cbda37-1651-4f46-9bc1-d89cb86e8d46)
출발역과 도착역을 선택하면 날짜 및 인원 입력 가능. 해당 열차 정보 조회 후 좌석 선택 가능

![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/2a33c393-10cd-4fa5-a13b-4962430f4115)
KCP결제 API사용하여 가상결제 기능 구현

### 5. 관리자 기능
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/a8457ec7-636e-43c8-9553-c9bea506c5fa)
<데이터 입력 페이지>
관리자 계정으로 로그인 시 상단바에 데이터입력, 데이터조회 기능 활성화
각각의 입력칸에는 Ajax로 중복확인 기능 구현.
menu데이터는 가게 정보 검색을 위한 팝업창 출력.
이미지는 32자리 고유ID 생성하여 DB에 입력, resources폴더에 저장


![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/bacfad49-a316-41b4-b3be-9453fcbde4cf)
<데이터 조회 페이지>
데이터 조회 페이지에서는 놀거리, 먹거리 정보 조회, 삭제 가능

### 6. 마이페이지
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/b22bf9f5-5385-4fb2-8067-a11f3f4b496e)
회원정보 수정, 놀거리, 먹거리 저장 목록 조회 및 삭제기능, 예매내역 확인 기능 구현

### 7. Kakao Map API, Sweet Alert2 사용
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/9f8eae17-3d9f-4916-a6c0-44bdee8d5903)
<br>
위치정보가 필요한 페이지에는 KaKaoMap API 사용하여 위치 정보 출력, Sweet Alert2 사용하여 Alert창 디자인

---
## ✏️ ERD
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/3729cfec-8286-484f-ad97-d10e0fcd1b92)

--- 
## 🤼‍♂️Author
Team Leader : 🐯Lee Yeon Woo

Backend : 🐺 Park MinSeo

Frontend: 🐱 Lim Jeong Eun

