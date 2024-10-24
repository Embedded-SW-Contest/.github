# 안전지킴이 
## LG Embedded 자동차 모빌리티 부문

# :oncoming_automobile: UWB 기반 골목길 교통사고 안전 서비스

<img src="https://github.com/user-attachments/assets/33c6fc02-52ea-4d9e-8b47-d9e0a2157748" alt="작품 이미지" width="500"/>

## 프로젝트 소개

- 좁은 길을 지나는 차량과 사람의 위치 기반 교통사고 방지 서비스이다.
- UWB 통신을 이용하여 운전자에게 보이지 않는 사각지대에서 접근하는 보행자가 <br> 주행 중인 차량에 가까워지면 운전자 및 보행자에 위험을 알린다.

<br>

## 시스템 차량 탑재

|외부|내부|
|--|--|
|![외부](https://github.com/user-attachments/assets/771d9410-9ce4-4183-8868-b68bb817257d)|![운전석](https://github.com/user-attachments/assets/470ec5cb-fb2b-436b-bd35-7de4fb5298ac)| 

<br>

## 충돌 감지시 알림

|차량|안드로이드|
|--|--|
|![차량](https://github.com/user-attachments/assets/53a661e4-7d08-42da-989e-169b54325579)|![안드로이드](https://github.com/user-attachments/assets/bc348165-383a-4c6b-a226-b7ff979427ac)| 

- UWB 통신으로 보행자를 발견하면 지도에 보행자를 띄우고, 보행자가 차량으로 접근 할 경우 라즈베리파이 UI에 Alert
- UWB 통신으로 보행자를 향해 달려오는 차량을 발견하면 안드로이드에 Alert

  <br>

## 결과 영상 링크 

- 

<br>

## 시스템 구성도

![시스템 구성도](https://github.com/user-attachments/assets/d08e80d2-735f-452e-80a7-c464e6cff90e)

- 시스템은 Embedded System, Client-Server, Application으로 나뉜다.
- Embedded System
  - 외부 센서 : GPS 및 차량 양옆의 거리를 측정해줄 라이다
  - 알람 센서 : 진동 센서 및 Alert를 띄울 Display
  - Companion Computer : Embedded System의 통제를 담당하는 Raspberry pi
  - UWB Module : 차량에 탑재되어 Android와 UWB 통신
- Client-Server
  - UI : Naver Map API를 통해 차량의 현재 위치와 보행자의 위치를 지도에 띄우고 충돌 감지시 Alert
  - Server: REST API를 통해 데이터를 주고받을 수 있는 기능을 제공
- Application
  - Android : Jetpack 라이브러리를 이용한 Estimote SDK로 개발, 비콘과의 UWB 통신을 통해 차량 감지

<br>

## 작동 흐름도

![작동 흐름도](https://github.com/user-attachments/assets/a4b3d897-dad1-447f-a5cb-ed6d30118271)

## 팀원 소개

|                                           팀장                                           |                                         팀원                                          |                                         팀원                                          |                                                                                     
| :------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: | 
| <img src="https://github.com/user-attachments/assets/e4593759-cdc7-41c6-ad17-7bc376cbaba8" width=200px alt="이준호"/> | <img src="https://github.com/user-attachments/assets/ab14c911-fe5e-41c4-9c72-7bc30584ba3c" width=200px alt="이정원"/> | <img src="https://github.com/user-attachments/assets/0a7ec33f-0044-4552-a98e-132eae98942f" width=200px alt="윤정빈"/> |
|                           이준호                          |                           이정원                            |                           윤정빈                            |
|                           프로젝트 총괄 <br> 임베디드 소프트웨어 개발 <br> node.js 서버 개발                         |                           임베디드 소프트웨어 개발 <br> 차량용 디스플레이 UI 개발 <br> 안드로이드 어플리케이션 개발                            |                           임베디드 소프트웨어 개발 <br> 안드로이드 어플리케이션 개발 <br> 형상 관리                            |
