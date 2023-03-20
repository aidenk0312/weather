날씨 일기 프로젝트
이 프로젝트는 날짜와 일기 내용을 CRUD 할 수 있는 RESTful API를 제공합니다. 또한, 매일 자정에 OpenWeatherMap API를 사용하여 서울의 현재 날씨 데이터를 수집하고, 이를 DB에 저장합니다.

1. Swagger
- API 문서: Swagger UI를 통해 볼 수 있습니다. http://localhost:8080/swagger-ui.html에 접속하면 사용 가능합니다.

2. 일기 생성: 선택한 날짜와 일기 내용을 입력하여 DB에 일기를 저장합니다.
- URL: /create/diary
- Method: POST
- Parameters:
  > date (날짜, yyyy-MM-dd 형식)
  > text (일기 내용, 문자열)

3. 일기 조회: 선택한 날짜의 모든 일기 데이터를 가져옵니다.
- URL: /read/diary
- Method: GET
- Parameters:
  > date (날짜, yyyy-MM-dd 형식)

4. 기간별 일기 조회: 선택한 기간 중의 모든 일기 데이터를 가져옵니다.
- URL: /read/diaries
- Method: GET
- Parameters:
  > startDate (조회할 기간의 첫 번째 날, yyyy-MM-dd 형식)
  > endDate (조회할 기간의 마지막 날, yyyy-MM-dd 형식)

5. 일기 수정: 선택한 날짜의 일기 내용을 수정합니다.
- URL: /update/diary
- Method: PUT
- Parameters:
  > date (날짜, yyyy-MM-dd 형식)
  > text (일기 내용, 문자열)

6. 일기 삭제: 선택한 날짜의 일기 데이터를 삭제합니다.
- URL: /delete/diary
- Method: DELETE
- Parameters:
  > date (날짜, yyyy-MM-dd 형식)
