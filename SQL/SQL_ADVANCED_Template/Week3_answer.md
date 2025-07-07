## 문제 1

> **🧚미정이는 지역별로 가장 인기 있는 식당 2곳씩을 뽑기 위해 다음과 같은 UNION ALL 기반 쿼리를 작성했습니다.**

~~~sql
(
  SELECT region, restaurant_name, review_count
  FROM Restaurants
  WHERE region = '서울'
  ORDER BY review_count DESC
  LIMIT 2
)
UNION ALL
(
  SELECT region, restaurant_name, review_count
  FROM Restaurants
  WHERE region = '부산'
  ORDER BY review_count DESC
  LIMIT 2
)
UNION ALL
(
  SELECT region, restaurant_name, review_count
  FROM Restaurants
  WHERE region = '대구'
  ORDER BY review_count DESC
  LIMIT 2
);
~~~

> **쿼리는 잘 작동하긴 하지만, 지역을 더 추가해달라는 권택이의 부탁으로 UNION ALL 블록을 계속 추가하게 되어 관리가 어려울 것 같아서 힘들어하고 있었습니다. 여러분들은 이 쿼리를 윈도우 함수로 변경하여 더 쉽게 리팩토링을 하려고 합니다. 미정이를 도와서 UNION ALL 없이 RANK( ) 또는 ROW_NUMBER( ) 윈도우 함수를 사용해, 각 지역별로 리뷰 수가 가장 많은 상위 2개 식당을 추출하는 쿼리를 작성해보세요.**



~~~sql
# 정답 코드 
SELECT region, restaurant_name, review_count
FROM (
  SELECT region, restaurant_name, review_count,
         ROW_NUMBER() OVER (PARTITION BY region ORDER BY review_count DESC) AS rn
  FROM Restaurants
) ranked
WHERE rn <= 2;

# 풀이 설명
# ROW_NUMBER() OVER (PARTITION BY region ORDER BY review_count DESC) 한 줄을 활용하여 
# 외부 쿼리에서 WHERE rn <= 2 조건을 통해 각 지역의 상위 2개의 식당을 한 줄로 풀이할 수 있다. 
# 이렇게 하면 지역이 많아지더라도 (수십, 수백 개 지역이 생겨도) UNION ALL 없이 자동으로 모든 지역에 대해 상위 2개만 추출할 수 있다. 
~~~





