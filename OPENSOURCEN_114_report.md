# 오픈소프트웨어(N) 1_14조 조별과제 report

## 목차

1. 추진배경-임하늘, 강다현
2. 기술 분석-임하늘, 강다현
3. 유사서비스 분석- 임하늘, 강다현
4. 사용 오픈소스(설명, 선정이유, 상세분석, 활용계획)- 전원
5. 서비스 구현을 위한 설계-정재훈
6. GUI 소개- 곽범석, 전세정
7. API 정의-곽범석, 국승빈, 권화경, 정세영
8. DFD-곽범석, 국승빈, 권화경, 정세영
9. 마무리 및 소감

## 추진배경

## 기술분석

## 유사서비스 분석

## 사용 오픈소스

## React

사용자 인터페이스 구축을 위한 자바스크립트 라이브러리

페이스북(메타)에서 개발한 프론트앤드 개발 오픈소스 자바스크립트 라이브러리로 SPA(Single Page Application)를 개발할 수 있다. 기존에 리액트를 비롯한 페이스북의 대부분의 오픈소스 프로젝트는 “BSD + Patents” 라이선스를 사용하였으나, 2017년 7월 Apache 재단이 “BSD + Patents” 라이선스를 사용하는 모든 코드를 금지하면서 결국 MIT 라이선스로 변경하였다.

### 특징

-   SPA 개발

    Single Page Application의 약자로 여러 개의 페이지로 구성된 전통적인 웹페이지와는 달리, 한 개의 페이지로 이루어진 애플리케이션이다. 사용자가 다른 페이지를 요청할 경우 전통적인 웹페이지에서는 서버에서 새로운 html을 받아 출력한다. 그러나 SPA에서는 페이지를 구성하는 모든 정보를 시작 시 한 번에 가져오고, 사용자가 다른 페이지를 요청하면 코드를 실행한다. 사용자 입장에서는 페이지 요청 시 딜레이(새로고침했을 때 빈 화면 같은)가 없다는 점이 가장 크게 체감될 것이다.

-   컴포넌트 기반

    웹사이트에는 헤더, 내비게이션 등 재사용이 가능한 부분이 많이 보인다. 이것들을 컴포넌트라는 묶음으로 만들어 레고를 조립하듯 하나의 페이지에 뗐다 붙였다 할 수 있다. 예를 들어 메인 페이지에서는 헤더 컴포넌트와 메인 컴포넌트, 푸터 컴포넌트를 사용하도록 하고, 사용자가 검색 페이지를 클릭하면 메인 컴포넌트 대신 검색 컴포넌트로 바꿔주는 것이다.

-   Virtual DOM

    DOM 이란 자바스크립트가 이용할 수 있도록 웹페이지 태그들을 트리구조로 만든 객체 모델이다. 전통적인 웹페이지에서는 특정 요소에 접근하여 10개의 변화를 주면 랜더 트리가 10번 수정되어 렌더링 된다. 그러나 리액트는 가상 돔을 사용하여 이전의 가상돔과 비교하고 바뀐 부분이 있는지 체크한다. 바뀐 부분이 있다면 그 부분만 실제 DOM에 적용하여 렌더링 횟수를 줄이게 된다.

### 비슷한 웹 프레임워크

-   Angular
-   Veu
-   Svelte

## Redux

상태관리를 위한 자바스크립트 라이브러리

MIT 라이센스를 사용한다.

### 사용하는 이유

-   Props Drilling 해결

      <div style="display:flex; flex-direction:row">
      <img src="./image/props_drilling.png">
      <img src="./image/store.png">
      </div>

    SPA는 기본적으로 여러 컴포넌트를 만들고 이를 조합하는 구조이다. 예를 들어 헤더, 메인, 검색창 등을 각각의 컴포넌트로 만들고 필요할 때 불러오는 방식이다. 위의 사진에서 만약 Root에서 G 컴포넌트까지 정보를 보내고 싶다면 A 컴포넌트와 E 컴포넌트를 거쳐야 된다. 지금은 4레벨의 트리구조지만 만약 더 작은 단위까지 컴포넌트를 쪼갠다면 거쳐야 될 컴포넌트가 많아질 것이고, 유지 보수에 어려움이 생긴다. Redux를 사용하면 상태 값을 컴포넌트에 종속시키지 않고, 밖에서 관리할 수 있다.

## 서비스 구현을 위한 설계

## GUI 소개

## API 정의
| Description | Method | URI | Request Header / Body |
| --- | --- | --- | --- |
| 회원 등록 | POST | /user/{userId} | name (String),<br>id (String),<br>password (String) |
| 회원 정보 조회 | GET | /user/{userId} | auth_token (String) |
| 회원 정보 수정 | PUT | /user/{userId} | auth_token (String) |
| 회원 탈퇴 | DELETE | /user/{userId} | auth_token (String) |
| 로그인 | POST | /session | id (String),<br>password (String) |
| 로그아웃 | DELETE | /session | auth_token (String) |
| 모든 그림 조회 | GET | /pictures |  |
| 그림 생성 | POST | /pictures | auth_token (String),<br>keyword(String) |
| 특정 그림 정보 조회 | GET | /pictures/{pictureId} |  |
| 특정 그림 정보 수정 | PUT | /pictures/{pictureId} | auth_token (String) |
| 특정 그림 삭제 | DELETE | /pictures/{pictureId} | auth_token (String) |

## DFD

## 마무리 및 소감
