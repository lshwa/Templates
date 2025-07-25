# ML 3주차 정규과제

📌ML 정규과제는 매주 정해진 **유튜브 강의 영상을 통해 머신러닝 이론을 학습**한 후, 해당 내용을 바탕으로 **실습 문제를 풀어보며 이해도를 높이는 학습 방식**입니다. 

이번주는 아래의 **ML_3rd_TIL**에 명시된 유튜브 강의를 먼저 수강해 주세요. 학습 중에는 주요 개념을 스스로 정리하고, 이해가 어려운 부분은 강의 자료나 추가 자료를 참고해 보완해주세요. 과제까지 다 작성한 이후에 Github를 과제 시트에 제출해주시면 됩니다.



**(수행 인증샷은 필수입니다.)** 

> 주어진 과제를 다 한 이후, 인증샷이나 따로 코드를 깃허브에 정리하여 제출해주세요.



## ML_3rd_TIL

### 의사결정나무모델 1 (모델 개요, 예측 나무)

### 의사결정나무모델 2 (분류 나무, Information Gain)

<br>



## 주차별 학습 (Study Schedule)

| 주차   | 공부 범위                              | 완료 여부 |
| ------ | -------------------------------------- | --------- |
| 0주차. | 선형 회귀 (Linear Regression) (1)      | ✅         |
| 1주차  | 선형 회귀 (Linear Regression) (2)      | ✅         |
| 2주차  | 로지스틱 회귀 (Logistic Regression)    | ✅         |
| 3주차  | 결정 트리 (Decision Tree)              | ✅         |
| 4주차  | 앙상블 : 랜덤 포레스트 (Random Forest) | 🍽️         |
| 5주차  | 주성분 분석 (PCA)                      | 🍽️         |
| 6주차  | K - 평균 군집화                        | 🍽️         |

<!-- 여기까진 그대로 둬 주세요-->



---

# 01. 의사결정나무모델 1 (모델 개요, 예측 나무)

```
✅ 학습 목표 :
* 의사결정나무 (Decision Tree) 모델의 개념과 동작 방식을 이해할 수 있다.
* 예측나무 (Regression Tree)의 분할 방식과 예측 방법을 이해할 수 있다.
* 의사결정나무 모델의 데이터 분할 과정과 그 목적을 이해할 수 있다. 
```

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



# 02. 의사결정나무모델 2 (분류 나무, Information Gain)

```
✅ 학습 목표 :
* 분류나무(Classification Tree) 모델의 구조와 동작 원리를 이해할 수 있다. 
* 불순도 지표(Gini, Cross-Entropy, Misclassification Rate)와 Information Gain의 개념을 이해할 수 있다.
* 분류나무 모델의 한계와 과적합 문제를 이해할 수 있다. 
```

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->



<br>
<br>

# 과제

> **와인 품질 데이터셋을 사용하여 레드 / 화이트 와인을 분류하는 결정 트리 모델을 만들어봅시다. `plot_tree`함수로 트리 구조를 시각화하고, 와인 종류를 구분하는 가장 중요한 상위 2개의 분기 규칙이 무엇인지 주피터 노트북을 통해 작성해보세요.**



~~~
과제 가이드
1. 데이터 불러오기 및 준비
- 와인 품질 데이터셋 사용
- 레드 / 화이트를 이진 분류로 설정한다. (예시) red = 0, white = 1

2. 모델 학습
- from sklearn.tree import DecisionTreeClassifier, plot_tree 라이브러리 사용
- model.fit(X_train, y_train)으로 학습을 한다. 

* 힌트
- 트리의 루트노드로부터 상위 2~3개의 분기가 가장 핵심적인 변수입니다.
~~~



<br>

### 🎉 수고하셨습니다.