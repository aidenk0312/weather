### 날씨 일기 프로젝트
 - 날짜와 일기 내용을 CRUD 할 수 있는 RESTful API를 구현
 - OpenWeatherMap API를 사용하여 매일 자정에 서울의 현재 날씨 데이터를 수집하고 DB에 저장하는 기능 구현

## 1. Swagger
 - API 문서: Swagger 통해 구현

## 2. 구현 방법
 - Java Spring Boot를 사용하여 RESTful API를 구현
 - 일기와 날씨 데이터를 저장하고 조회하기 위해 JPA를 사용
 - API 문서는 Swagger를 사용하여 자동 생성
 - 날씨 데이터를 수집하기 위해 OpenWeatherMap API를 사용
 - 데이터의 동시성을 보장하기 위해 트랜잭션 처리를 적용

## 3. API 목록 및 상세 내용:
 - [x] 일기 생성: 선택한 날짜와 일기 내용을 입력하여 DB에 일기를 저장
 
   (URL: /create/diary, Method: POST, Parameters: date, text)

 - [x] 일기 조회: 선택한 날짜의 모든 일기 데이터를 가져오기
 
   (URL: /read/diary, Method: GET, Parameters: date)
   
 - [x] 기간별 일기 조회: 선택한 기간 중의 모든 일기 데이터를 가져오기
 
   (URL: /read/diaries, Method: GET, Parameters: startDate, endDate)
   
 - [x] 일기 수정: 선택한 날짜의 일기 내용을 수정
 
   (URL: /update/diary, Method: PUT, Parameters: date, text)
   
 - [x] 일기 삭제: 선택한 날짜의 일기 데이터를 삭제
 
   (URL: /delete/diary, Method: DELETE, Parameters: date)
