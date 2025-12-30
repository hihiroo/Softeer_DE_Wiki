# 데이터 오버뷰
## 1. 파일 포맷
### Raw 데이터 샘플 (mtcars.csv)
```
"","mpg","cyl","disp","hp","drat","wt","qsec","vs","am","gear","carb"
"Mazda RX4",21,6,160,110,3.9,2.62,16.46,0,1,4,4
"Mazda RX4 Wag",21,6,160,110,3.9,2.875,17.02,0,1,4,4
"Datsun 710",22.8,4,108,93,3.85,2.32,18.61,1,1,4,1
...
```
| "" | mpg | cyl | disp | hp | drat | wt | qsec | vs | am | gear | carb |
|:--:|:---:|:---:|:----:|:--:|:----:|:--:|:---:|:--:|:--:|:----:|:----:|
|"Mazda RX4"|21|6|160|110|3.9|2.62|16.46|0|1|4|4|
|"Mazda RX4 Wag"|21|6|160|110|3.9|2.875|17.02|0|1|4|4|
|"Datsun 710"|22.8|4|108|93|3.85|2.32|18.61|1|1|4|1|

* 파일 형식: CSV
* 첫 번째 행은 컬럼명(header)

<br>

## 2. 컬럼 오버뷰
| Column | Description | Type | Notes |
|:-:|:-:|:-:|:-:|
| mpg | Miles per (US) gallon | float | 연비 지표, 값이 클수록 연비가 좋음 |
| cyl | Number of cylinders | int | 보통 4, 6, 8 → 범주형으로 해석 가능 |
| disp | Displacement (cu.in.) | float | 엔진 배기량, 엔진 크기 지표 |
| hp | Gross horsepower | float | 엔진 출력(마력) |
| drat | Rear axle ratio | float | 가속/고속 주행 특성에 영향 |
| wt | Weight (lb / 1000) | float | 차량 무게 (1000 파운드 단위) |
| qsec | 1/4 mile time | float | 가속 성능 지표 (낮을수록 빠름) |
| vs | Engine type (0 = V-shaped, 1 = straight) | int | 이진 범주형 변수 |
| am | Transmission (0 = automatic, 1 = manual) | int | 이진 범주형 변수 |
| gear | Number of forward gears | int | 기어 수, 범주형으로 해석 가능 |
| carb | Number of carburetors | int | 연료 공급 장치 개수 |

<br>

## 3. 데이터 개요
* **본 데이터는 자동차의 성능 관련 지표를 제공하는 데이터셋으로 분석됨.**
* 각 행은 하나의 차량 모델을 나타내며, 첫 번째 컬럼인 차량 이름이 행 식별자 역할을 하고 있음
* 수치형 변수와 범주형 변수가 혼합된 구조로, 일부 범주형 변수는 0 또는 1로 인코딩된 변수임