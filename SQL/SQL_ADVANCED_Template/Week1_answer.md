## 문제 1

> **🧚예린이는 고객별로 얼마나 많은 주문을 하는지 분석하기 위해, 고객의 주문 목록에 주문 순서를 표시하는 쿼리를 작성해보았습니다. 이때 주문일 순서대로 각 고객의 주문 번호를 매기기 위해 윈도우 함수를 활용했습니다.**

~~~sql
SELECT customer_id, order_id, order_date,
       ROW_NUMBER() OVER (PARTITION BY customer_id ORDER BY order_date) AS order_rank
FROM Orders;
~~~

> **이번에는 예린이에게 "윈도우 함수를 쓰지 않고 동일한 결과를 만들어보라"는 미션을 받았습니다. 예린이는 이 작업을 어떻게 해야할지 막막합니다. 예린이를 도와 ROW_NUMBER() 윈도우 함수 없이 동일한 결과를 서브쿼리나 JOIN을 사용해서 작성해보세요.**



~~~sql
SELECT o1.customer_id, o1.order_id, o1.order_date,
       (
         SELECT COUNT(*)
         FROM Orders o2
         WHERE o2.customer_id = o1.customer_id
           AND o2.order_date <= o1.order_date
       ) AS order_rank
FROM Orders o1;

# 다음과 같이 서브쿼리로 해결이 가능하다. 현재 행에 대해서 같은 고객의 주문 중 현재 주문일보다 같거나 이전인 주문 ㅜ를 세어 순위처럼 사용한다. order_date가 같은 경우에는 순위가 같아질 수 있어, ROW_NUMBER() 와는 정확히 같지는 않다. 
~~~

