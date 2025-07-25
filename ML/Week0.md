# ML 0주차 정규과제

📌ML 정규과제는 매주 정해진 **유튜브 강의 영상을 통해 머신러닝 이론을 학습**한 후, 해당 내용을 바탕으로 **실습 문제를 풀어보며 이해도를 높이는 학습 방식**입니다. 

이번주는 아래의 **ML_0th_TIL**에 명시된 유튜브 강의를 먼저 수강해 주세요. 학습 중에는 주요 개념을 스스로 정리하고, 이해가 어려운 부분은 강의 자료나 추가 자료를 참고해 보완해주세요. 과제까지 다 작성한 이후에 Github를 과제 시트에 제출해주시면 됩니다.



**(수행 인증샷은 필수입니다.)** 

> 주어진 과제를 다 한 이후, 인증샷이나 따로 코드를 깃허브에 정리하여 제출해주세요.



## ML_0th_TIL

### 수치예측, 범주예측

### 머신러닝 모델 학습 프로세스

### 선형회귀모델 1 (개요, 모델가정)

### 선형회귀모델 2 (파라미터 추정, 최소제곱법)

<br>

<!-- TIL에서 나와있는 강의 사이에 있는 과제에 해당이 되지 않는 강의도 내용이 연속적으로 진행하기 때문에 수강하시면 이해하기 쉬우실 것입니다. -->



## 주차별 학습 (Study Schedule)

| 주차   | 공부 범위                              | 완료 여부 |
| ------ | -------------------------------------- | --------- |
| 0주차. | 선형 회귀 (Linear Regression) (1)      | ✅         |
| 1주차  | 선형 회귀 (Linear Regression) (2)      | 🍽️         |
| 2주차  | 로지스틱 회귀 (Logistic Regression)    | 🍽️         |
| 3주차  | 결정 트리 (Decision Tree)              | 🍽️         |
| 4주차  | 앙상블 : 랜덤 포레스트 (Random Forest) | 🍽️         |
| 5주차  | 주성분 분석 (PCA)                      | 🍽️         |
| 6주차  | K - 평균 군집화                        | 🍽️         |

<!-- 여기까진 그대로 둬 주세요-->



---

# 01. 수치해석, 범주예측

```
✅ 학습 목표 :
* 수치예측과 범주예측의 차이를 이해할 수 있다.
* 다변량 데이터의 개념을 이해할 수 있다. 
* 예측 모델링의 목적을 강의에서 제시한 예시를 통해서 파악할 수 있다. 
```

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



# 02. 머신러닝 모델 학습 프로세스

```
✅ 학습 목표 :
* 다변량 데이터에서 X와 Y의 관계를 이해할 수 있다.
* 머신러닝 모델이 파라미터(w1,w2 등)를 찾는 과정임을 이해할 수 있다.
* 비용함수 최소화를 통해 파라미터를 추정하는 원리를 이해할 수 있다. 
```

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->

<!-- 강의에서 공식이 많이 나오는데 공식에 대한 이해보다는 (나중에 배울 예정) 학습 프로세스에 대한 개념 중심적으로 공부해주세요.-->




# 03. 선형회귀모델 1 (개요, 모델 가정)

```
✅ 학습 목표 :
* 선형회귀모델의 개념과 목적을 이해할 수 있다.
* 확정적 관계와 확률적 관계의 차이를 이해할 수 있다.
* 선형회귀모델의 가정과 파라미터 추정의 의미를 이해할 수 있다. 
```

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->




# 04. 선형회귀모델 2 (파라미터 추정, 최소제곱법)

```
✅ 학습 목표 :
* 파라미터 추정의 목적과 과정(비용함수 최소화)을 이해할 수 있다.
* Least Square(최소제곱법)의 원리를 이해할 수 있다.
* 잔차(Residual)와 확률 오차(ε)의 차이를 구분할 수 있다. 
```

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->




<br>
<br>

# 과제

> **보스턴 주택 가격 데이터셋을 사용하여 주택 가격 예측 모델을 훈련 후, `model.coef_`값을 확인하고, 어떤 특성이 주택 가격에 가장 큰 부정적 / 부정적 영향을 미치는지 분석하여 설명하는 주피터 노트북을 작성하세요.**



~~~
과제 가이드
1. Boston Housing Dataset 소개
- sklearn.datasets.load_boston()으로 불러올 수 있는 데이터셋입니다. 
- 각 컬럼은 주택 가격에 영향을 줄 수 있는 다양한 특성을 나타냅니다. (예 : 평균 방 개수, 범죄율 등)

2. 선형회귀 모델 훈련
- sklearn.linear_model.LinearRegression( )을 사용해서 훈련할 수 있습니다.
- model.fit(X, y)를 사용하세요.

3. model.coef_ 해석 방법
- model.coef_ 는 각 특성(feature)의 계수(coefficient)를 의미합니다.
- 계수가 양수이면 그 특성이 클수록 주택 가격이 올라가는 것을 의미하고, 계수가 음수이면 그 특성이 클수록 주택 가격이 내려간다는 것을 의미합니다. 

4. 결과 분석 포인트
- model.coef_ 의 절댓값이 큰 변수가 가격에 더 큰 영향을 미칩니다. 
- 어떤 특성이 가장 긍정적인 영향을 미치고, 어떤 특성이 가장 부정적인 영향을 미치는지 찾아보세요.
- (X축 : 특성이름, Y축 : 계수 값) 을 사용하여 시각화를 사용해서 표현해도 좋습니다. 
~~~



<br>

### 🎉 수고하셨습니다.