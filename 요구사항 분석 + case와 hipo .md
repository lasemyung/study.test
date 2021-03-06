# 요구사항 분석

- 개발 대상에 대한 **`사용자의 요구사항을 이해하고 문서화`** 하는 과정
- 사용자 요구의 타당성과 비용, 일정, 제약 등을 설정한다



## 구조적 분석 기법

- 자료의 흐름과 처리를 중심으로 하는 요구사항 분석 방법
- 하향식 방법을 사용하여 시스템을 세분화 할 수 있다
- 구조적 분석 기법 도구
  1.  자료 흐름도
  2. 자료 사전
  3. 소단위 명세서
  4. 개체 관계도
  5. 상태 전이도
  6. 제어 명세서



### 자료 흐름도 ( data flow diagram )

- 자료의 흐름 및 변환 과정과 기능을 도형 중심으로 기술하는 방법
- 자료 흐름도 기본 기호
  1. 프로세스 : 자료를 변환시키는 시스템의 한 부분 ( 처리 과정 )을 나타내며 처리, 기능, 변환, 버블 이라고 함
  2. 자료 흐름 :  자료의 이동이나 연관관계를 나타냄
  3. 자료 저장소 : 시스템에서의 자료 저장소 ( 파일, 데이터베이스 )를 나타냄
  4. 단말 : 시스템과 교신하는 외부 개체로, 입력 데이터가 만들어지고 출력 데이터를 받음



### 자료 사전 ( DD )

- 자료 흐름도에 있는 자료를 자세히 정의하고 기록한 것
- 데이터를 설명하는 데이터로 **`메타 데이터`**라고도 한다

- 자료 사전 기호
  1.  =  :  정의, ~로 되어 있다
  2.  플러스 : 자료의 연결 , and
  3.  () : 생략 가능한 자료
  4.  [] : 자료의 선택 or
  5.  {} : 자료의 반복
  6.  ** : 주석



# 요구사항 분석용 CASE ( 자동화 도구 )

- 요구사항을 자동으로 분석하고 요구사항 분석 명세서를 기술하도록 개발된 도구
- 대표적인 분석용 CASE
  1.  SADT : **`블록 다이어 그램 채택한 자동화 도구`**, 시스템 정의, 소프트웨어 요구사항 분석, 설계
  2.  SREM = RSL/REVS:  TRW사가 실시간 처리 소프트웨어 시스템에서 요구사항을 명확히 기술하도록 할 목적으로 개발한 도구
  3. PSL/PSA : PSL과 PSA를 사용하는 자동과 도구
  4. TAGS :  시스템 공학 방법 응용에 대한 자동 접근 방법, **`개발 주기 전 과정에 이용 가능`**한 자동화 도구



# HIPO

- 시스템의 분석 및 설계, 문서화에 사용되는 기법으로 시스템 실행 과정인 입력, 처리, 출력의 기능을 표현
- 하향식 소프트웨어 개발을 위한 문서화 도구
- 기능과 자료의 의존 관계를 동시에 표현 가능
- 기호, 도표 등을 사용하므로 보기 쉽고 이해하기도 쉽다
- HIPO Chart
  1. 가시적 도표 ( visual table of contents)
  2. 총체적 도표(Overview Diagram)
  3. 세부적 도표(Detail Diagram)
