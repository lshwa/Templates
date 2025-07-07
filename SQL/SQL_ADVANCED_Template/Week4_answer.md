## 문제 1

> **🧚승화는 어떤 기업의 조직 구조를 분석하는 SQL 쿼리를 작성하고 있습니다. 각 직원은 상위 관리자 ID(manager_id)를 가지며, 조직도는 같은 Employees 테이블 내에서 계층적으로 연결됩니다. 승화는 최상위 관리자부터 각 사원까지의 계층 깊이(depth)를 계산하고자 다음과 같은 SELF JOIN 기반 쿼리를 시도했습니다.** 

~~~sql
SELECT e1.id, e1.name, e2.name AS manager_name
FROM Employees e1
LEFT JOIN Employees e2 ON e1.manager_id = e2.id;
~~~

> **쿼리를 잘 작성했다고 생각을 했지만, 막상 실행을 해보니 1단계 매니저까지만 추적할 수 있어 계층 구조의 전체를  표현하는데 한계가 존재했습니다. 이에 여러분에게 다음과 같은 미션을 요청합니다. WITH RECURSIVE를 활용하여  최상위 관리자부터 시작해 각 직원까지의 조직 구조 계층 깊이(depth)를 구하고, 결과를 depth가 높은 순으로 정렬하세요.**



~~~sql
WITH RECURSIVE org_structure AS (
    -- Anchor member: 최상위 관리자 (manager_id가 NULL)
    SELECT id, name, manager_id, 0 AS depth
    FROM Employees
    WHERE manager_id IS NULL

    UNION ALL

    -- Recursive member: 상위 직원에 연결된 하위 직원 탐색
    SELECT e.id, e.name, e.manager_id, os.depth + 1
    FROM Employees e
    JOIN org_structure os ON e.manager_id = os.id
)
SELECT *
FROM org_structure
ORDER BY depth DESC, id;

# 문제에서 처럼 SELF JOIn을 하면 한 단계만 추적이 가능하다. 
# 따라서 정답 코드와 같이 재귀 CTE를 사용하면 여러 계층을 따라가는데 더 적합하다. 
~~~



