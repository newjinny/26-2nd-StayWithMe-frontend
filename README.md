# 🗺 PROJECT_STAYWITHME | 스테이위드미

스테이위드미 UI/UX 메인 서비스

1. 각 숙소에 대한 정보를 접근하기 위한, Feed list 형식을 제공합니다.
2. 정보의 접근성을위해, pagination을 통해 list로 분할하여 보여줍니다.
3. 각 숙소에 대한 DetailPage 내에서 숙소에 대한 정보 및 이미지를 확인할 수 있으며 Info-Extension을 Carousel-Slider를 통해 보여줍니다.

- 사이트 링크 :

# 🚀 TEAM_STAYWITHME | 스테이위드미

- 영상 : 

## 👫 팀원

- Front-end: 최병현, 지연비 , 신유진
- Back-end: 권은경, 이찬규

## 개발 기간

- 기간: 2021년 11월 15일 ~ 2021년 11월 26일(12일간)

## 적용 기술

- Front-end: React(Funiction-Component)\_reactr-router-dom(V6), 
Styled-Components, JavaScript(ES6)
- Back-end: Django, Python, MySQL, jwt, bcrypt, AWS(EC2, RDS)
- 협업툴: Trello, Slack, Notion, Github, dbdiagram, postman

## 구현 기능 및 개인 역할

> **최병현**: InfoList Page

- 서버에서 받아 온 데이터 형식(data-type)에 따라 각 숙소 정보가 담긴 Feed를 일정 크기만큼 mapping 하여 list 형식으로 보여줍니다.
- 서버에 각기 다른 offset 값을 path query에 넣음으로써, 사용자가 page 버튼을 누를 때마다 다른 list를 볼 수 있도록 Pagination(화면 분할) 기능을 구현하였습니다.
- 조건에 따라 현재 path 값을 parsing하여 각기 다른 query 조건값이 계속 붙게되도록 하거나 업데이트되도록 하는 queryModule를 따로 생성하고 이를 프로젝트에서 전연적으로 쓰일 수 있도록 하였습니다.
- dayPicker 라이브러리를 사용하여 사용자가 check_in / check_out 날짜를 선택하여 해당 기간에 맞는 숙소 리스트들을 볼 수 있도록 기능을 구현하였습니다.
- 최소 금액과 최대 금액을 한번에 취합하여 서버에 해당 데이터를 보낼 수 있도록 Input type인 range 기능을 사용하여 Slider 기능을 구현하였습니다.

> **지연비**: Login/Register, PaymentPage 

[Login/Register]
- 카카오 Open API를 이용한 소셜로그인 기능 구현
- 로그인시 백엔드에서 발행한 Token을 Local storage에 저장

[PaymentPage]
- useSearchParams(), fetch()를 사용하여 이전 페이지에서 선택한 정보들을 불러오는 기능 구현
- 체크박스 전체선택/전체해제 구현
> **신유진**: DetailPage
- Navigation Bar(네비게이션 바) 구현
  - React Router v6의 Link 컴포넌트를 활용하여 SPA 구현
- 숙소 Detail Page 구현
  - React-slick 라이브러리 사용하여 캐러셀 구현
  - 슬라이드 index를 state로 관리(라이브러리 미사용)하여 캐러셀 구현
  - Info Page에서 선택한 예약 날짜를 쿼리스트링으로 변환하고, 이를 API를 통해 호출하여 Detail Page에 렌더링
  - Array.map() 메서드를 사용하여 API로 불러온 호텔 정보를 이미지 캐러셀에 렌더링



## 소감 및 후기

> **최병현** : 서버에서 조건에 맞는 데이터 값을 가져오기 위고 화면에 랜더링되도록 현재 path 값의 query 부분을 지속적으로 parsing하고 업데이트하기 위한 모듈의 로직을 만드는 것은 상당히 어려웠다. 
해당 모듈의 내부 로직을 수 많은 조건문과 정규 표현식을 사용하여 최종적으로 코드가 무엇(What?)을 하는 지에 대해서 불명확하게 된 점이 아쉬웠다. 다음 프로젝트 때는 useSearchParams와 같은 내부 기능을 사용하여 query값을 좀 더 효율적으로 parsing할 수 있는 로직을 구현해보고 싶다는 생각이 들었다.

> **지연비**: (소감 및 후기)
시간의 한계로 인해 마지막에 결제페이지의 data를 백엔드로 post하는 로직을 완성하지 못한 부분이 아쉽다.
다음 프로젝트에서는 결제페이지와 마이페이지를 맡아서 페이지 간의 데이터 전송과 프론트, 백엔드 사이의 데이터 송수신에 대해 좀 더 알아보고 싶다.

> **신유진** : 캐러셀을 라이브러리 사용하는 방법과 미사용하는 방법 두 가지 방법으로 구현해 내는 방법을 배울 수 있었다. Info Page에서 선택한 날짜를 렌더링 하는 것은 구현해 냈지만 날짜를 선택 할 수 있는 달력 기능을 구현하지 못해서 조금 아쉬웠다. 기회가 된다면 공부해서 추가구현 해보고 싶다.

## 레퍼런스

- 이 프로젝트는 <u>[스테이폴리오](https://www.stayfolio.com/)으로 만들었습니다.
- 실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다.
