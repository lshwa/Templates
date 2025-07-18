### **문제 1**

> **🧚권택이는 고객의 이메일을 필터링하는 작업을 하고 있습니다. 모든 고객 중 이메일 도메인이 @gmail.com 또는 @naver.com인 고객만 추출하고자 합니다. REGEXP를 활용하여 쿼리를 작성해보세요.**

```
SELECT *
FROM customers
WHERE email REGEXP '(@gmail\\.com|@naver\\.com)$';
```

1. > 위 쿼리가 어떤 의미인지 설명하고, LIKE로 동일한 결과를 내는 방법도 함께 제시해보세요.

2. > email이 빈 문자열이거나 NULL인 경우는 어떻게 처리해야 할지 고민해보세요.



~~~
1. 쿼리설명 
	•	REGEXP: 정규표현식을 기반으로 조건을 걸 때 사용하는 연산자
	•	'(@gmail\\.com|@naver\\.com)$' 의미:
	•	@gmail\\.com 또는 @naver\\.com 으로 끝나는 문자열 ($는 문자열의 끝)
	•	\\.는 실제 마침표(.)를 의미하기 위해 이스케이프 처리
	
2. 
SELECT *
FROM customers
WHERE (email REGEXP '(@gmail\\.com|@naver\\.com)$')
  AND email IS NOT NULL
  AND email <> '';
~~~





> **🧚운영팀장인 지민이는 학회원 데이터에서 핸드폰 번호 형식을 점검하는 업무를 맡았습니다. 핸드폰 번호는 반드시 010으로 시작하고, 중간과 끝은 각각 4자리 숫자로 구성되어야 하며, 각 구간은 하이픈(-)으로 구분되어야 합니다. 예: 010-1234-5678 **
>
> **올바른 형식을 따르지 않는 번호를 가진 고객 목록을 찾아내기 위해 SQL의 REGEXP 기능을 사용하려고 합니다. 아래 조건에 맞는 고객 목록을 출력하는 쿼리를 작성해주세요.**

- 예시 테이블

| **student_id** | **name** | **phone_number** |
| -------------- | -------- | ---------------- |
| 1              | Anna     | 010-1234-5678    |
| 2              | Brian    | 011-1234-5678    |
| 3              | Cindy    | 01012345678      |
| 4              | David    | 010-123-5678     |
| 5              | Elsa     | 010-9999-8888    |

- 기대 출력 결과

| **student_id** | **name** | **phone_number** |
| -------------- | -------- | ---------------- |
| 2              | Brian    | 011-1234-5678    |
| 3              | Cindy    | 01012345678      |
| 4              | David    | 010-123-5678     |

> 문제 조건 
>
> - 형식이 **정확히** 010-XXXX-XXXX (X는 숫자, 총 4자리)인 경우만 통과
> - **정규 표현식을 사용하여 필터링**
> - 올바르지 않은 형식만 조회
> - 테이블 명은 Student로 해주세요.



~~~sql
SELECT *
FROM Student
WHERE phone_number NOT REGEXP '^010-[0-9]{4}-[0-9]{4}$';
~~~





