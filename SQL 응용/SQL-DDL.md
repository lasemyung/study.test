# SQL - DDL

- DDL은 DB 구조, 데이터 형식, 접근 방식 등 DB를 구축하거나 수정할 목적으로 사용하는 언어

- 번역한 결과가 데이터 사전이라는 특별한 파일에 여러개의 테이블로 저장

- DDL의 3가지 유형

  | CREATE | SCHEMA, DOMAIN, TABLE, VIEW, INDEX를 정의함 |
  | ------ | ------------------------------------------- |
  | ALTER  | TABLE에 대한 정의를 변경하는데 사용함       |
  | DROP   | SCHEMA, DOMAIN, TABLE, VIEW, INDEX를 삭제함 |
  |        |                                             |

  

### CREATE SCHEMA

- CREATE SHCEMA는 스키마를 정의하는 명령문이다

- 표기 형식

  ```sql
  CREATE SCHEMA 스키마명 AUTHORIZATION 사용자_ID;
  ```



### CREATE DOMAIN

- CREATE DOMAIN은 도메인을 정의하는 명령문

- 표기형식

  ```sql
  CREATE DOMAIN 도메인명 [AS] 데이터_타입
  	   [DEFAULT 기본값]
  	   [CONSTRAINT 제약조건명 CHECK (범위값)]
  ```

- 데이터 타입 : sql에서 지원하는 데이터 타입

- 기본값 : 데이터를 입력하지 않았을 때 자동으로 입력되는 값

  ```sql
  CREATE DOMAIN SEX CHAR(1) 정의된 도메인 이름이 'SEX'이며 문자형이고 크기는 1자이다
  DEFAULT '남' 도메인 SEX를 지정한 속성의 기본값은 '남'
  CONSTRAINT VAILD-SEX CHECK (VALUE IN ('남','여')) SEX를 지정한 속성에는 '남','여' 중 하나의 값만을 지정할 수 있다
  ```



### CREATE TABLE

- 테이블을 정의하는 명령문

- 표기형식

  ```SQL
  CREATE TABLE 테이블명
  	(속성명 데이터_타입 [DEFAULT 기본값] [NOT NULL], ...
  	[, PRIMARY KEY(기본키_속성명, ...)]
  	[, UNIQUE(대체키_속성명, ...)]
  	[, FOREIGN KEY(외래키_속성명, ...)]
  			REFERENCES 참조테이블(기본키_속성명, ...)]
  			[ON DELETE 옵션]
  			[ON UPDATE 옵션]
  	[, CONSTRAINT 제약조건명] [CHECK (조건식)];
  ```

- ADD : 새로운 속성(열)을 추가할 때 사용한다
- ALTER :  특정 속성의 DEFAULT 값을 변경할 때 사용한다
- DROP COLUMN : 특정 속성을 삭제 할 때 사용한다

```sql
ALTER TABLE 학생 ADD 학년 VARCHAR(3);
ALTER TABLE 학생 ALTER 학번 VARCHAR(10) NOT NULL;
```



### DROP

- DROP은 스키마, 도메인 , 기본 테이블, 뷰 테이블, 인덱스, 제약 조건 등을 제거하는 명령문

- 표기 형식

  ```sql
  DROP SCHEMA 스키마명 [CASCADE | RESTRICT];
  DROP DOMAIN 도메인명 [CASCADE | RESTRICT];
  DROP TABLE 테이블명 [CASCADE | RESTRICT];
  DROP VIEW 뷰명 [CASCADE | RESTRICT];
  DROP INDEX 인덱스명 [CASCADE | RESTRICT];
  DROP CONSTRAINT 제약조건명 ;
  ```

- CASCADE : 제거할 요소를 참조하는 다른 모든 개체를 함께 제거한다
- RESTRICT : 다른 개체가 제거할 요소를 참조 중일 때는 제거를 취소한다

