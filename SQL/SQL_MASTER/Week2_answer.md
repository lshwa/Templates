## 문제 1

> **🧚다음 쿼리는 조건에 따라 다른 결과를 출력하는 구문입니다. 아래 빈칸에 들어갈 적절한 SQL 키워드를 채우세요.**

~~~sql
SELECT member_id, name,
       ( ______
           ______ join_date IS NULL ______ '미가입',
           ______ join_date IS NOT NULL ______ '가입완료'
       ______ ) AS join_status
FROM Member
______ name;
~~~

> **또한, 이 쿼리는 무엇을 하기 위해 작성된 것인지도 간단히 작성해주시면 됩니다.**



~~~sql
SELECT member_id, name,
       ( CASE
           WHEN join_date IS NULL THEN '미가입',
           WHEN join_date IS NOT NULL THEN '가입완료'
       END ) AS join_status
FROM Member
ORDER BY name;
~~~

~~~
위 쿼리는 '회원 이름'을 가나다 순으로 정렬하면서 가입 여부를 구분하는 쿼리이다. 
~~~



