# SQL_ADVANCED 1주차 정규 과제 

📌**SQL_ADVANCED 정규과제**는 매주 정해진 주제에 따라 **MySQL 공식 문서 또는 한글 블로그 자료를 참고해 개념을 정리한 후, 프로그래머스 SQL 문제 3문제**와 **추가 확인문제**를 직접 풀어보며 학습하는 과제입니다. 

이번 주는 아래의 **SQL_ADVANCED_1st_TIL**에 나열된 주제를 중심으로 개념을 학습하고, 주차별 **학습 목표**에 맞게 정리해주세요. 정리한 내용은 GitHub에 업로드한 후, **스프레드시트의 'SQL' 시트에 링크를 제출**해주세요. 



**(수행 인증샷은 필수입니다.)** 

> 프로그래머스 문제를 풀고 '정답입니다' 문구를 캡쳐해서 올려주시면 됩니다. 

## SQL_ADVANCED_1st

### 14.20.2. Window Function Concepts and Syntax

### 14.20.1. Window Function Description

### 14.20.4. Named Window(Optional)

### 14.19.1. Aggregate Function Descriptions





### 공식 문서 활용 팁

>  **MySQL 공식 문서는 영어로 제공되지만, 크롬 브라우저에서 공식 문서를 열고 이 페이지 번역하기에서 한국어를 선택하면 번역된 버전으로 확인할 수 있습니다. 다만, 번역본은 문맥이 어색한 부분이 종종 있으니 영어 원문과 한국어 번역본을 왔다 갔다 하며 확인하거나, 교육팀장의 정리 예시를 참고하셔도 괜찮습니다.**





> 아래의 링크를 통해 *MySQL 공식문서*로 이동하실 수 있습니다.
>
> - 14.20.2. Window Function Concepts and Syntax : MySQL 공식문서 
>
> https://dev.mysql.com/doc/refman/8.0/en/window-functions-usage.html
>
> (한국어 버전)
>
> - 14.20.1. Window Function Descriptions : MySQL 공식문서
>
> https://dev.mysql.com/doc/refman/8.0/en/window-function-descriptions.html
>
> (한국어 버전)
>
> - 14.20.4. Named Windows - (Optional) : MySQL 공식문서
>
> https://dev.mysql.com/doc/refman/8.0/en/window-functions-named-windows.html
>
> (한국어 버전)
>
> - 14.19.1. Aggregate Function Descriptions : MySQL 공식문서 
>
> https://dev.mysql.com/doc/refman/8.0/en/aggregate-functions.html
>
> (한국어 버전)





## 🏁 강의 수강 (Study Schedule)

| 주차  | 공부 범위        | 완료 여부 |
| ----- | ---------------- | --------- |
| 0주차 | SubQuery & CTE   | ✅         |
| 1주차 | Window Functions | ✅         |
| 2주차 |                  | 🍽️         |
| 3주차 |                  | 🍽️         |
| 4주차 |                  | 🍽️         |
| 5주차 |                  | 🍽️         |
| 6주차 |                  | 🍽️         |

<br>



## LeetCode 문제 

https://leetcode.com/problems/department-top-three-salaries/

> Department Top Three Salaries (LeetCode) : DENSE_RANK(), PARTITION BY

https://leetcode.com/problems/consecutive-numbers/

> Consecutive Numbers (LeetCode) : LAG

https://leetcode.com/problems/last-person-to-fit-in-the-bus/

> Last Person to Fit in the Bus (LeetCode) : SUM() OVER 



문제를 푸는 다양한 방법이 존재하지만, **윈도우 함수를 사용하여 해결하는 방식에 대해 고민해주시길 바랍니다.** 



<!-- 여기까진 그대로 둬 주세요-->

---

 # 1. Window Function Concepts and Syntax

~~~
✅ 학습 목표 :
* 윈도우 함수와 일반 집계 함수의 차이에 대해 설명할 수 있다.
* 윈도우 함수의 기본 개념과, OVER(), PARTITION BY, ORDER BY, ROWS BETWEEN 등 문법을 사용할 수 있다. 
~~~

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



# 2. Window Function Description

~~~
✅ 학습 목표 :
* MySQL에 지원하는 윈도우 함수들에 대해 이해하고 설명할 수 있다. 
* 순위함수, 이동함수, 누적 집계 함수, 통계 함수에 대해 설명할 수 있다.
~~~

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



<!-- 14.20.4. Named Windows 는 Option 입니다. 그래도 읽고 정리해주신다면 그대는 정말 .. 인정-->

# 3. Aggregate Function Descriptions

~~~
✅ 학습 목표 :
* 일반집계 함수 목록을 윈도우 함수처럼 사용할 수 있다. 
* 집계함수와 윈도우 함수의 차이를 확실히 이해하고 설명할 수 있다. 
~~~

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



<br>

<br>

---

# 확인문제

## 문제 1

> **🧚예린이는 고객별로 얼마나 많은 주문을 하는지 분석하기 위해, 고객의 주문 목록에 주문 순서를 표시하는 쿼리를 작성해보았습니다. 이때 주문일 순서대로 각 고객의 주문 번호를 매기기 위해 윈도우 함수를 활용했습니다.**

~~~sql
SELECT customer_id, order_id, order_date,
       ROW_NUMBER() OVER (PARTITION BY customer_id ORDER BY order_date) AS order_rank
FROM Orders;
~~~

> **이번에는 예린이에게 "윈도우 함수를 쓰지 않고 동일한 결과를 만들어보라"는 미션을 받았습니다. 예린이는 이 작업을 어떻게 해야할지 막막합니다. 예린이를 도와 ROW_NUMBER() 윈도우 함수 없이 동일한 결과를 서브쿼리나 JOIN을 사용해서 작성해보세요.**

~~~
여기에 답을 작성해주세요!
~~~



<br>

### 🎉 수고하셨습니다.







