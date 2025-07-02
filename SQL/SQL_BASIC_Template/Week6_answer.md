# 확인문제

## 문제 1

> **🧚주영이는 다음 SQL 쿼리를 다트비 정규과제에 제출했다. 제출한 쿼리는 다음과 같고, 이 쿼리는 에러 메시지 없이 잘 수행하는 쿼리이다.**

~~~sql
# 주영이가 작성한 가독성 나쁜 SQL 

select u.name , o.OrderID
, p.ProductName ,od.Quantity ,od.UnitPrice 	from Users u	join Orders o on u.id = o.userId
join OrderDetails od on o.OrderID = od.orderID	join Products p on od.ProductID = p.ProductID
where u.region= 'Busan'			order by o.OrderID
~~~

> **이에 과제를 검사하던 지민이는 작성한 SQL을 보고 코드 리뷰를 진행하려고 했지만, 다음 쿼리를 보고 주영이에게 질문을 하였다. "주영아, 이 쿼리 가독성이 좀 안 좋은데 내가 고쳐도 괜찮을까? 가독성 좋게 SQL 가이드에 따라 정리해보려고 해"**
>
> 다음 SQL 쿼리를 **가독성 좋은 스타일로 다시 작성해보세요.** 



~~~sql
# 정답 쿼리 : 예약어는 대문자로, 컬럼 이름은 snake_case, alias는 명시적이고 의미있게, 쉼표는 줄 끝에 위치 
SELECT
    u.name,
    o.order_id,
    p.product_name,
    od.quantity,
    od.unit_price
FROM users AS u
JOIN orders AS o
    ON u.id = o.user_id
JOIN order_details AS od
    ON o.order_id = od.order_id
JOIN products AS p
    ON od.product_id = p.product_id
WHERE u.region = 'Busan'
ORDER BY o.order_id;
~~~

