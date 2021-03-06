# 보안 및 API

### 소프트웨어 개발 보안

- 보안 취약점을 최소화하여 보안 위협으로부터 안전한 소프트웨어를 개발하기 위한 일련의 보안 활동
- 데이터의 기밀성, 무결성, 가용성 등의 보안 요소를 충족시키는 것을 목표로 한다
- 정부에서 제공하는 소프트웨어 개발 보안 가이드를 참고하여 소프트웨어 개발 과정에서 점검해야 할 보안 항목들을 점검한다



### 소프트웨어 개발 보안 점검 항목

| 점검 항목                   | 내용                                                         |
| --------------------------- | ------------------------------------------------------------ |
| 세션 통제                   | 세션의 연결과 연결로 인해 발생하는 정보를 관리               |
| 입력 및 데이터 검증 및 표현 | 입력 데이터에 대한 유효성 검증 체계를 갖추고, 검증 실패 시 이를 처리할 수 있도록 코딩하는 것 |
| 보안 기능                   | 인증, 접근제어, 기밀성, 암호화                               |
| 시간 및 상태                | 동시 수행을 지원하는 병렬 처리 시스템이나 다수의 프로세스가 동작하는 환경에서 시간과 실행 상태를 관리하여 시스템이 원활히 동작하도록 코딩하는 것 |
| 에러 처리                   | 소프트웨어 실행 중 발생할 수 있는 오류들을 사전에 정의하여 에러로 인해 발생할 수 있는 문제들을 예방하는 것 |
| 코드 오류                   | 개발자들이 코딩 중 실수하기 쉬운 형 변환 자원의 반환 등을 고려하며 코딩 |
| 캡슐화                      | 속성과 데이터를 처리하는 함수를 하나의 객체로 묶어 코딩하는 것 |
| API 오용                    | API를 잘못 사용하거나 보안에 취약한 API를 사용하지 않도록 고려하여 코 |
|                             |                                                              |



### API ( Application Programming Interface )

- API는 응용 프로그램 개발 시 운영체제나 프로그래밍 언어 등에 있는 라이브러리를 이용할 수 있도록 규칙 등으 정의 해 놓은 인터페이스를 의미한다

- 라이브러이에 있는 다양한 기능들을 손쉽게 이용 할 수 있도록 도와주므로 효율적인 개발이 가능하다

- 누구나 무료로 사용할 수 있게 공개된 API를 Open API라고 한다

- API의 종류

  ```
  Windows API, 단일 유닉스 규격(SUS), Java API, 웹 API
  ```

  

