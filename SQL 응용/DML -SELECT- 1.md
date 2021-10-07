# DML -SELECT- 1

일반 형식

```sql
SELECT [PREDICATE] [테이블명.]속성명 [AS 별칭][, [테이블명.]속성명,...]
[그룹함수(속성명)[AS 별칭]]
[, Windows함수 OVER (PARTITION bY 속성명1, 속성명2,...
					ORDER BY 속성명3, 속성명4)]
FROM 테이블명[,테이블명,...]
[WHERE 조건]
[GROUP BY 속성명, 속성명, ...]
[HAVING 조건]
[ORDER BY 속성명 [ASC/ DESC]];
```



### 기본 검색

- SELECT 절에 원하는 속성을 지정하여 검색한다

- 사원 테이블에 모든 튜플을 검색하세요

  ```sql
  SELECT * FROM 사원;
  SELECT 사원.* FROM 사원;
  SELECT 이름,부서,생일,주소,기본급 FROM 사원
  SELECT 사원.이름,사원.부서,사원.주소,사원.기본급 FROM 사원;
  ```

  

### 조건 지정 검색

- WHERE 절에 조건을 지정하여 조건에 만족하는 튜플만 검색

  EX) 사원 테이블에서 기획부의 모든 튜플을 검색하세요

  ```sqlite
  SELECT *
  FROM 사원
  WHERE 부서 = '기획';
  ```

  EX) 사원 테이블에서 기획 부서에 근무하면서 대흥동에 사는 사람의 튜플을 검색하세요

  ```sql
  SELECT *
  FROM 사원
  WHERE 부서 = '기획' AND 주소 '대흥동';
  ```

  EX) 사원 테이블에서 성이 김인 사람의 튜플을 검색하세요

  ```SQL
  SELECT *
  FROM 사원
  WHERE 이름 LIKE "김%";
  ```

  EX) 사원 테이블에서 '생일'이 01/01/69 에서 12/31/73 사이인 튜플을 검색하세요

  ```SQL
  SELECT *
  FROM 사원
  WHERE 생일 #01/01/69# AND #12/31/73#; '도 가능'
  ```



### 정렬 검색

- ORDER BY 절에 특정 속성을 지정하여 지정된 속성으로 자료를 정렬하여 검색한다.

  EX) 사원 테이블에서 주소를 기준으로 내림차순 정렬시켜 상위 2개 튜플만 검색하세요

  ```sql
  SELECT TOP2 *
  FROM 사원
  ORDER BY 주소 DESC;
  ```

  EX) 사원 테이블에서 부서를 기준으로 오름차순 정렬하고, 같은 부서에 대해서는 이름을 기준으로 내림차순 정렬시켜 검색해주세요

  ```SQL
  SELECT *
  FROM 사원
  ORDER BY 부서 ASC, 이름 DESC
  ```



### 하위 질의

- 조건절에 주어진 질의를 먼저 수행하여 그 검색 결과를 조건절의 피연산자로 사용한다

  EX) 취미가 나이트댄스인 사원의 이름과 주소를 검색하세요

  ```SQL
  SELECT 이름, 주소
  FROM 사원
  WHERE 이름 = (SELECT 이름 FROM 여가활동 WHERE 취미 ='나이트댄스');
  ```

  EX) 취미활동을 하지 않는 사원들을 검색하세요

  ```sql
  SELECT *
  FROM 사원
  WHERE 이름 NOT IN ( SELECT 이름 FROM);
  ```

  EX) 취미활동을 하는 사원들의 부서를 검색하세요

  ```SQL
  SELECT 부서
  FROM 사원
  WHERE EXISTS ( SELECT 이름 FROM 여가활동 WHERE 여가활동.이름 = 사원.이름 );
  ```

  

  ### 복수 테이블 검색

- 여러 테이블을 대상으로 검색을 수행한다

- EX) 경력이 10년 이상인 사원의 이름, 부서, 취미, 경력을 검색하세요

  ```SQL
  SELECT 사원.이름, 사원.부서, 여가활동.취미, 여가활동.경력
  FROM 사원, 여가활동
  WHERE 여가활동.경력 >= 10 AND 사원.이름 = 여가활동.이름
  ```

  
