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

