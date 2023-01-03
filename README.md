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

3. ORDER BY 문
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

5. GROUP BY 문
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

***

6. IS [NOT] NULL
* WHERE 문에 사용
* NULL 값만 찾거나 아닌것만 찾거나

***

7. HAVING 문
* GROUP함수로 집계된 데이터에 조건을 줄 때 사용한다.
* 연산자는 GROUP BY 연산에 의하여 나누어진 데이터들을 다시 걸러주기 위해서 사용하고,
	제2의 WHERE조건문이라고 할 수 있으며 조건문에서 그룹함수를 사용가능하다.
* HAVING 문 다음에는 SELECT-LIST에서 사용한 컬럼과 그룹함수를 
    사용한 컬럼에 대해서만 조건을 줄 수 있다.

* [내부 수행(호출) 순서]
> * SELECT 		-5
> * FROM		-1
> * WHERE		-2
> * GROUP BY	-3
> * HAVING		-4
> * ORDER BY	-6
* [실행 순서]	중요!!
> * SELECT		-6
> * FROM		-1
> * WHERE		-2
> * GROUP BY	-3
> * HAVING		-4
> * ORDER BY	-5

***

8. WITH ROLLUP
* 그룹 총합, 부분 소개
> * ROLLUP 연산자는 GROUP BY 문과 함께 사용되며
	GROUP BY 문에서 명시한 컬럼 순서대로 추가적인 요약정보를 단계적으로 만들어준다

***

9. CUBE = 소계, 총계 
* GROUP BY 문과 함께 사용되며 GROUP BY 문에서 명시한 전체 컬럼에
	대하여 추가적인 요약 정보를 단계적으로 만들어 준다.(MY SQL에는 없음)

10. GROUPING 
* GROUPING 함수는 그룹 기준에서 고려하지 않은 부분 총계인 경우에 1을 리턴하고,
	그렇지 않은 경우 0을 리턴한다.

***

