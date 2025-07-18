# SQL_MASTER 1주차 정규 과제 

## Week 1 : 실전용 SQL 미리 맛보기 

📌**SQL_MASTER 정규과제**는 매주 MySQL Workbench 툴을 활용하여 **직접 데이터베이스를 설계하고 실습하는 프로젝트 기반 과제**입니다. 

이번 주는 아래의 **SQL_MASTER_1st_TIL**에 나열된 주제를 중심으로 개념을 학습하고, 주차별 **학습 목표**에 맞게 정리해주세요. 정리한 내용은 GitHub에 업로드한 후, **스프레드시트의 'SQL' 시트에 링크를 제출**해주세요. 



> ✅ **과제 제출 시 반드시 “Workbench 실습 화면 (캡처)” 를 첨부해주세요!**
>
> - 테이블 생성, 수정, 삭제 명령이 실행된 화면 또는 결과가 확인되는 캡처를 첨부합니다.
> - Github에 정리하는 실습 TIL 링크를 **스프레드시트 'SQL_MASTER' 시트에 제출**해주세요.



## SQL_MASTER_1st_TIL

## 2장. 실전용 SQL 미리 맛보기

### 01. 건물을 짓기 위한 설계도 : 데이터베이스 모델링

### 02. 데이터베이스 시작부터 끝까지 

### 03. 데이터베이스 개체



## 🏁 주차별 학습 (Study Schedule)

| 주차  | 공부 범위                  | 완료 여부 |
| ----- | -------------------------- | --------- |
| 0주차 | **데이터베이스와 SQL**     | ✅         |
| 1주차 | **실전용 SQL 미리 맛보기** | ✅         |
| 2주차 | **기본, 고급 DML 복습**    | 🍽️         |
| 3주차 | **테이블과 뷰**            | 🍽️         |
| 4주차 | **인덱스**                 | 🍽️         |
| 5주차 | **스토어드 프로시져**      | 🍽️         |
| 6주차 | **SQL 파이썬 연결하기**    | 🍽️         |

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

# 01. 실전용 SQL 미리 맛보기

~~~
✅ 학습 목표 :
* 데이터베이스 모델링의 개념을 파악할 수 있다. 
* 전반적인 데이터베이스 구축 절차를 이해할 수 있다. 
* 데이터베이스 개체인 인덱스, 뷰, 스토어드 프로시저에 대해 미리 이해할 수 있다. 
~~~

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



## 인증사진 

> **1. 책 83p의 실행결과를 올려주세요**

<!-- 이 주석을 지우고 여기에 이미지를 첨가하세요. -->

<br>

> **2. 책 97p의 실행결과의 이미지를 올려주세요.**

<!-- 이 주석을 지우고 여기에 이미지를 첨가하세요. -->

<br>



<br>

---

# 확인문제

## 문제 1

> **🧚다음 테이블을 생성하는 명령어를 실행했더니 오류가 발생했습니다. 오류의 원인이 되는 부분을 찾고, 그 이유를 설명하세요. 그리고 정상적으로 실행되기 위해 어디를 바꿔야 하는지 설명하세요.**

~~~sql
CREATE TABLE Member (
    member_id INT PRIMARY KEY,
    name VARCHAR(50),
    join_date NULL,
    email VARCHAR(100)
);
~~~



~~~
여기에 답을 작성해주세요.
~~~



## 문제 2

> **🧚책에서는 `DELIMTER //` 를 사용했습니다. 만약 `DELIMITER &&` 또는 `DELIMITER !!`와 같이 다른 기호를 사용해도 실행이 될까요? 만약 된다면, 그 이유도 함께 설명해주세요.**

~~~sql
DELIMITER //
CREATE PROCEDURE testProc()
BEGIN
    SELECT 'Hello, MySQL!';
END //
DELIMITER ;
~~~



~~~
여기에 답을 작성해주세요.
~~~



<!-- 위의 2문제는 책 뒤 챕터에서 더 자세히 다룰 내용입니다. 첫번째 문제는 자료형에 집중해주시면 되고, 두번째 문제는 프로시저의 DELIMITER에 대해 자료를 찾아서 공부한 것들도 같이 넣어주세요. -->



# 참고자료

**MySQL Workbench 에 대한 설명이 잘 적혀있는 강의입니다. 혹시 아직 설치를 하시지 못하셨다면 아래 링크의 01, 02편 영상을 보시고 설치 진행해주시면 됩니다. 이미 들으셨던 분은 이번 주차에는 03,04 편을 시청해주시면 됩니다.**

> 책을 보고 이해가 잘 되시면 꼭 보시지는 않으셔도 됩니다.



[참고 외부자료는 여기를 클릭해주세요.](https://www.youtube.com/playlist?list=PL_RECGqDS3ieZFybjCx0kTYkPK-TioY1S)

<br>

### 🎉 수고하셨습니다.







