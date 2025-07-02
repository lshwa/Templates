## 문제 1

> **🧚예린이는 최근 여러 주문 데이터를 분석하는 업무를 맡게 되었습니다. 특정 고객의 주문 이력을 분석하기 위해, 다음과 같이 최근 30일간 주문만 필터링한 CTE를 사용해 쿼리를 작성했습니다.**

~~~sql
WITH RecentOrders AS (
  SELECT *
  FROM Orders
  WHERE order_date >= DATE_SUB(CURDATE(), INTERVAL 30 DAY)
)
SELECT customer_id, COUNT(*) AS recent_order_count
FROM RecentOrders
GROUP BY customer_id;
~~~

> **그런데 예린이는 "이 쿼리를 WITH 없이, 서브쿼리 방식으로 바꿔서 실행해보라" 는 피드백을 받았고, 서브쿼리로 작성해보려 했지만 익숙하지 않아 SQL_ADVANCED를 듣는 학회원분들에게 도움을 요청하고 있습니다. 예린이의 쿼리를 WITH 없이 서브쿼리로 변환해보세요. 그리고 두 방식의 차이점을 설명해보고, 각각의 장단점을 정리해보세요**



**정답**

- 서브쿼리 방식으로 변환한 쿼리

~~~sql
SELECT customer_id, COUNT(*) AS recent_order_count
FROM (
  SELECT *
  FROM Orders
  WHERE order_date >= DATE_SUB(CURDATE(), INTERVAL 30 DAY)
) AS RecentOrders
GROUP BY customer_id;
~~~

- WITH절과 서브쿼리의 차이점

~~~
WITH 방식은 복잡한 로직을 논리적으로 분리하고 가독성을 높일 수 있다는 장점이 존재한다. 그리고 CTE 이름을 여러 번 사용할 수 있기 때문에 성능적으로도 서브쿼리보다 뛰어나다고 얘기할 수 있다. 
서브쿼리는 중첩되면 읽기 어려워지고, 재사용이 불가능하기에 다시 작성해줘야한다. 쿼리의 길이가 짧은 곳에서는 CTE보다는 성능적으로 좋을 수 있어도, 보편적으로는 CTE(WITH) 방식이 더 좋다. 
~~~

