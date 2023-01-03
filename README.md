# TIL006
## MYSQL

***

1. 비교연산
* '>, >=, <, <=, =, !=, <>'
* WHERE문에 조건으로 사용
    * SELECT  ---> 3
    * FROM    ---> 1
    * WHERE   ---> 2   결과가 TRUE 일때 작동

***

2. 문자열 
* WHERE ~ LIKE 'A%'
    * 'A%': 맨앞이 A 
    * '%A': 맨뒤가 A
    * '%AA%': A가 두개 들어간것
    * 'A%B': 맨앞이 A 맨뒤가 B
    * '_A%': 앞에서 두번째가 A 
    * '%A_': 뒤에서 두번쨰가 A

***

3. ORDER BY
* 
    * SELECT 칼럼1, 칼럼2, 칼럼3
    * FROM 테이블
    * ORDER BY 칼럼 1;
* 
    * SELECT 칼럼1, 칼럼2, 칼럼3
    * FROM 테이블
    * ORDER BY 1;
*   order by문에서 ASC / DESC 를 컬럼명 뒤에 사용하여 오름차순 / 내림차순으로 표현

***

4. 집계함수
* 집계함수 (컬럼명) : NULL 처리 안됨
    * SUM()
    * AVG()
    * COUNT()
    * MAX()
    * MIN()
    * STD()
    * ...
* 일반적으로 select문 뒤에 컬럼 대신 사용가능

***

5. GROUP BY
* 1.
    * GROUP BY 문 다음에는 데이터를 구분짓기위한 표현식으로
	* 해당 테이블의 컬럼명이나 변수 값 등이 올 수 있으며 
    * 그룹함수를 사용한 형태는 올 수 없다< GROUP BY AVG(SAL) 안됨>
* 2.
    * SELECT-LIST에는 GROUP BY문에 명시된 표현식과
    * 그외 그룹함수를 사용한 표현식만이 올 수 있다.(* 안됨)
* 3.
    * 출력된 결과를 정렬하기 위해 ORDER BY 문을 사용하면 된다.
    * 단, ORDER BY 문 다음에는 SELECT-LIST에서 명시된 컬럼 또는
    * 표현식과 컬럼의 별칭(ABCD), 컬럼 번호 등만 사용 
