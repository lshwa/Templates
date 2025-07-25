## 문제 1.

> **🧚Q. 예린이는 연애 관련 컨텐츠를 제작하는 회사의 지인에게 부탁을 받아 '서울의 인기있는 데이트 코스 TOP 3'를 정하기 위해 각 장소에 대한 온라인 후기 평점을 수집했습니다. 온라인 후기 평점은 아래와 같습니다.**

| **장소**        | **평균 평점** | **평점 수** | **평점 편차 (표준편차)** |
| --------------- | ------------- | ----------- | ------------------------ |
| 익선동 한옥마을 | 4.8           | 1,000       | 0.3                      |
| 성수동 카페거리 | 4.7           | 950         | 0.9                      |
| 한강 공원       | 4.6           | 1,200       | 1.4                      |

> **예린이는 평균 평점을 보고, "오! 익선동 한옥마을이 가장 높고 안정적이니까 무조건 1위네" 라고 말하고 이를 지인에게 전달했습니다.**
>
> **위 사례에서 예린이의 접근 방식은 데이터 문해력 관점에서 타당한지, 각 장소의 평점에 담긴 의미를 활용해 비교해보세요.**



~~~
예린이는 평균 평점만을 기준으로 '익선동 한옥마을'이 1위라고 판단했지만, 이는 데이터 문해력 관점에서 타당하지 않다. 평균은 전체 경향을 보여주는 지표일 뿐, 후기의 분포나 안정성을 파악하려면 '편차'를 함께 고려해야 한다. 

	- 장소별 해석 -
1. 익선동 한옥마을 (평균 4.8, 편차 0.3) 
- 평균이 높고 편차도 작기 때문에, 후기 대부분이 매우 긍정적일 가능성이 크다
- 리뷰가 안정적이고 일관되게 좋다고 볼 수 있다.

2. 성수도 카페거리 (평점 4.7, 편차 0.9)
- 평균은 비슷하지만 편차가 익선동 한옥마을에 비해 더 크다. 이는 일부 극단적으로 낮거나 높은 평점이 섞여 있을 가능성이 존재한다. 
- 방문객 경험이 양극화되어 있을 수 있다. 

3. 한강 공원 (평점 4.6, 편차 1.4)
- 평균은 가장 낮고, 편차는 가장 크다. 사람들마다 느끼는 바가 매우 다르다고 할 수 있다. 
- 독특하거나 호불호가 갈리는 장소일 수 있다. 
~~~

