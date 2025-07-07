# SQL_MASTER 0주차 정규 과제 

## Week 0 : DDL 실습(CREATE / ALTER / DROP)

📌**SQL_MASTER 정규과제**는 매주 MySQL Workbench 툴을 활용하여 **직접 데이터베이스를 설계하고 실습하는 프로젝트 기반 과제**입니다. 

본 주차는 DDL (Data Definition Language) 문법을 이해하고 실습하는 것을 목표로 합니다. 



> ✅ **과제 제출 시 반드시 “Workbench 실습 화면 (캡처)” 를 첨부해주세요!**
>
> - 테이블 생성, 수정, 삭제 명령이 실행된 화면 또는 결과가 확인되는 캡처를 첨부합니다.
> - Github에 정리하는 실습 TIL 링크를 **스프레드시트 'SQL_MASTER' 시트에 제출**해주세요.



## SQL_MASTER_Week0

**실습 목표**

### 1. MySQL Workbench Tool 다운로드

### 2. DDL (CREATE / ALTER/ DROP)

- 나만의 테이블과 데이터베이스를 직접 생성해본다. 
- 테이블에 컬럼을 추가하거나 수정 /삭제 해본다. 
- 테이블을 안전하게 삭제해본다. 



**실습 가이드**

### 1. 데이터베이스 생성

- 이름 : master_week0
- 인코딩 : utf8mb4
- 캡처 : 데이터베이스 생성 완료 후 좌측 `Object Browser` 화면



### 2. 기본 테이블 생성

- 테이블명 : members 
- 컬럼 구성:
  - id (INT, PRIMARY KEY, AUTO_INCREMENT)
  - name (VARCHAR(50), NOT NULL)
  - email (VARCHAR(100), UNIQUE)
  - created_at (TIMESTAMP, DEFAULT CURRENT_TIMESTAMP)
- 캡처: *CREATE TABLE 실행 화면 및 Object Browser 내 테이블 생성 확인*



### 3. 테이블 수정 (ALTER 실습)

- 아래 컬럼을 추가해보세요:
  - phone_number (VARCHAR(20), NULL 허용)
- 다음 작업도 시도해보세요:
  - email 컬럼의 UNIQUE 제약 조건 제거
  - name 컬럼 이름을 full_name으로 변경
- 캡처: *ALTER TABLE 쿼리 및 변경 결과 확인 화면*



### 4. 테이블 삭제

- members 테이블을 DROP 해보세요.
- 캡처: *DROP 실행 쿼리 및 테이블 삭제 확인 화면*



## 🏁 주차별 학습 (Study Schedule)

| 주차  | 공부 범위                               | 완료 여부 |
| ----- | --------------------------------------- | --------- |
| 0주차 | DDL 실습                                | ✅         |
| 1주차 | DCL 실습                                | 🍽️         |
| 2주차 | DML 실습                                | 🍽️         |
| 3주차 | 저장 프로시저 작성 및 최적화            | 🍽️         |
| 4주차 | 함수 및 트리거 작성과 활용              | 🍽️         |
| 5주차 | 트랜잭션 관리 및 고급 데이터베이스 관리 | 🍽️         |
| 6주차 | 데이터베이스 정규화                     | 🍽️         |

<br>

<!-- 여기까진 그대로 둬 주세요-->

---

 # 1. DDL

~~~
✅ 학습 목표 :
* DDL 에 대해 설명할 수 있다. 
* CREATE / ALTER / DROOP 을 자유롭게 활용할 수 있다. 
~~~

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



<br>

<br>

---

# 확인문제





### 🎉 수고하셨습니다.







