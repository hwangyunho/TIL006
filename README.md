# TIL006
## MYSQL
1. 비교연산
- '>, >=, <, <=, =, !=, <>'

SELECT  ---> 3

FROM    ---> 1

WHERE   ---> 2   결과가 TRUE 일때

1. 문자열 
* WHERE ~ LIKE 'A%'
    * 'A%': 맨앞이 A 
    * '%A': 맨뒤가 A
    * '%AA%': A가 두개 들어간것
    * 'A%B': 맨앞이 A 맨뒤가 B
    * '_A%': 앞에서 두번째가 A 
    * '%A_': 뒤에서 두번쨰가 A