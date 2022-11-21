오픈소프트웨어(N) 1_14조 조별과제 report
======
목차
------
1. 추진배경-임하늘, 강다현
2. 기술 분석-임하늘, 강다현
3. 유사서비스 분석- 임하늘, 강다현
4. 사용 오픈소스(설명, 선정이유, 상세분석, 활용계획)- 전원
5. 서비스 구현을 위한 설계-정재훈
6. GUI 소개- 곽범석, 전세정
7. API 정의-곽범석, 국승빈, 권화경, 정세영
8. DFD-곽범석, 국승빈, 권화경, 정세영
9. 마무리 및 소감

추진배경
------

기술분석
------

유사서비스 분석
------

사용 오픈소스
------

서비스 구현을 위한 설계
------

GUI 소개
------

API 정의
| Description | Method | URI | Request Header / Body |
| --- | --- | --- | --- |
| 회원 등록 | POST | /user/{userId} | name (String),
id (String), 
password (String) |
| 회원 정보 조회 | GET | /user/{userId} | auth_token (String) |
| 회원 정보 수정 | PUT | /user/{userId} | auth_token (String) |
| 회원 탈퇴 | DELETE | /user/{userId} | auth_token (String) |
| 로그인 | POST | /session | id (String)
password (String) |
| 로그아웃 | DELETE | /session | auth_token (String) |
| 모든 그림 조회 | GET | /pictures |  |
| 그림 생성 | POST | /pictures | auth_token (String),
keyword(String) |
| 특정 그림 정보 조회 | GET | /pictures/{pictureId} |  |
| 특정 그림 정보 수정 | PUT | /pictures/{pictureId} | auth_token (String) |
| 특정 그림 삭제 | DELETE | /pictures/{pictureId} | auth_token (String) |
------

DFD
------

마무리 및 소감
------