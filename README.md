# _Tripick Main Page_


![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/7b7fd177-6fab-48c1-99c9-fbeb8d77d6e1)

---
## ✨ Description
```
기존 기차 예매 사이트 인터페이스의 불편함을 개선하고, 
놀거리와 먹거리 정보를 간편하게 Pick! 할 수 있는 사이트입니다. 
```


## 🔍 Overview
### _1.유저 회원가입 페이지_
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/79a7fcfd-e27d-4b13-8e7b-8586cece7210)
JavaScript 사용하여 중복체크 구현

### _2. 놀거리, 먹거리 해시태그 기능_
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/9d58926d-eca6-432c-bd79-7e1001e165bf)
- 원하는 지역과 해시태그 버튼을 누르면 AJAX를 통해 데이터를 검색하고, jQuery의 ‘.html()’ 
  메서드로 데이터가 출력됨.
- 모든 놀거리와 먹거리 데이터에는 테마 코드가 있음. 놀거리의 경우 계절, 함께하는 사람,
  목적별로 나눠지고 먹거리의 경우 일식, 양식, 한식, 카페 등으로 테마 코드가 정해져있음.
  해시태그를 클릭할 때마다 5자리 테마 코드가 완성되어 원하는 놀거리, 먹거리가 출력됨.
- 지역을 우선적으로 선택하도록 설계함. 지역을 선택하지 않고 해시태그 버튼을 누르면 지역 우선 
  선택 요청 알림 창이 출력됨.


### _3. 놀거리, 먹거리 상세정보 조회 페이지_
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/aa1ab3c1-ef47-4386-bcaf-97134d18b8fa)
- 저장 기능을 제공함. 북마크와 동일하며 저장기능은 JSTL의 c:if와 session을 활용하여 로그인이 되어있지 않으면 저장버튼 클릭 시 로그인 페이지로 이동함. 로그인이 되어있을 경우 ‘저장 완료되었습니다’ 를 출력하고, 이미 저장된 정보일경우 ‘이미 저장되어 있습니다’ 를 출력함.
- 해당 장소에 대한 리뷰를 남길 수 있음. 리뷰 작성 시 좋아요, 싫어요 버튼으로 추천수를 집계할 수 있음.
- 놀거리 상세보기 페이지의 경우 해당 놀거리 위치정보가 마커로 표시되며 주변 정보를 알 수 있음.
- 상세보기의 '예매하기' 기능을 통해 해당 즐길거리 근처 KTX역으로 간편하게 열차를 예매할 수 있음.


### _4. 기차 예매 기능_
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/c8cbda37-1651-4f46-9bc1-d89cb86e8d46)
출발역과 도착역을 선택하면 날짜 및 인원 입력 가능. 해당 열차 정보 조회 후 좌석 선택 가능

![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/2a33c393-10cd-4fa5-a13b-4962430f4115)
KCP결제 API사용하여 가상결제 기능 구현

### _5. 관리자 기능_
<데이터 입력 페이지>
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/a8457ec7-636e-43c8-9553-c9bea506c5fa)
###### 관리자 계정으로 로그인 시 JSTL의 c:if를 활용하여 관리자 전용 메뉴(데이터 입력, 데이터 조회, 블로그 작성)가 활성화됨.
- 데이터 입력 : ‘놀거리’, ‘먹거리’, ‘가게의 메뉴’ 데이터를 직접 넣을 수 있으며 메뉴정보는 가게의 하위 메뉴이므로 가게 코드 검색 기능(팝업창에서 AJAX와 jQuery의 ‘.html()’메서드 활용) 제공.
  모든 데이터에는 STRING 타입의 고유 코드와 사진이 필수임. 코드의 최댓값을 조회하여 형 변환 뒤 +1씩 더하여 고유코드를 만듦. 사진은 UUID메서드를 통해 랜덤 한 32자리코드+사진이름으로 DB와 resources폴더에 저장됨.
- 블로그 작성 : 즐길 거리를 소개하는 글을 작성할 수 있는 버튼이 활성화됨. 만약 작성된 블로그 글이 없는 즐길 거리의 경우 일반 사용자에게 블로그 바로 가기 버튼이 노출되지 않음. 


<데이터 조회 페이지>
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/bacfad49-a316-41b4-b3be-9453fcbde4cf)
- 데이터 조회 : 놀거리, 먹거리, 가게 메뉴의 모든 데이터를 조회 가능하고 각각의 데이터를 삭제할 수 있음. 외래 키로 지정된 각각의 데이터는 삭제 버튼을 누를 경우 하위 테이블의 데이터부터 차례대로 삭제됨.
- 해당 페이지에서 새로운 기능 테스트를 위한 버튼이 존재합니다. '테스트메인페이지 이동'을 클릭하면 반응형 웹페이지 구축 테스트 페이지로 이동합니다.

### _6. 마이페이지_
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/b22bf9f5-5385-4fb2-8067-a11f3f4b496e)
- 원하는 놀거리, 먹거리를 저장하여 마이페이지에서 JSTL의 c:forEach를 통해 저장한 장소를 출력하여 확인할 수 있음. 저장한 장소는 삭제도 가능함.
- 예매내역 확인 가능. 예매 상세보기 페이지에서는 예매취소가 가능하지만 승차시간이 지난 이후
부터는 예매취소가 불가능 하도록 설계함.


### _7. Kakao Map API, Sweet Alert2 사용_
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/9f8eae17-3d9f-4916-a6c0-44bdee8d5903)
- 카카오맵 API로 놀거리, 먹거리 페이지 최상단에서 검색기능을 지원함, 상세보기 페이지에서 해당 장소에 대한 정보가 마커로 표시되며, 주변 정보를 알 수 있음.
- Sweet Alert2 사용하여 Alert창 디자인

---
## ✏️ ERD
![image](https://github.com/MoongBan/Tripick_sources/assets/122944951/3729cfec-8286-484f-ad97-d10e0fcd1b92)

--- 
## 🤼‍♂️Author
Team Leader : 🐯Lee Yeon Woo

Backend : 🐺 Park MinSeo

Frontend: 🐱 Lim Jeong Eun

