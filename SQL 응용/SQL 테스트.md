# SQL 테스트

- SQL이 작성 의도에 맞게 원하는 기능을 수행하는지 검증하는 과정
- 단문 SQL은 SQL코드를 직접 실행한 후 결과를 확인하는 것으로 간단히 테스트 가능하다
- 절차형 SQL은 테스트 전에 생성을 통해 구문 오류나 참조 오류의 존재 여부를 확인한다
- 정상적으로 생성된 절차형 SQL은 디버깅을 통해 로직을 검증하고 결과를 통해 최정적으로 확인한다



### 단문SQL 테스트

- DDL,DML,DCL이 포함되어 있는 SQL과 TCL을 테스트하는 것으로 직접 실행하여 결과물을 확인
- DDL로 작성된 개체는 DESCRIBE 명령어를 이용하여 속성,자료형,옵션들을 확인가능
- DML로 변경한 데이터는 SELECT문으로 데이터의 정상적인 변경 여부를 확인 가능
- DCL로 설정된 사용자 권한은 사용자 권한 정보가 저장된 테이블을 조회하여 확인 가능



### 절차형 SQL 테스트

- 프로시저, 사용자 정희 함수, 트리거 등의 절차형 SQL은 디버깅을 통해 기능의 적합성 여부를 검증하고 실행을 통해 결과를 확인하는 테스트를 수행한다
- 많은 코드로 구성된 절차형 SQL의 특성상 오류 및 경고 메시지가 상세히 출력되지 않으므로 SHOW 명령어를 통해 오류 내용을 확인하고 문제를 수정한다
- 데이터 베이스에 변화를 줄 수 있는 SQL문은 주석으로 처리하고 출력문을 이용하여 화면에 출력하여 확인
- 디버깅이 완료되면 출력문을 삭제하고 주석 기호를 삭제 후 절차형 SQL을 실행하여 결과를 검토한다



