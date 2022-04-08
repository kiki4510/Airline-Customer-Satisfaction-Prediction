# Airline-Customer-Satisfaction-Prediction
Based on Kaggle Airline Customer Satisfaction Data 
## 문제정의
* 항공사 고객만족도에 영향을 끼치는 요인들을 살피고 만족과 불만족을 예측하는 분류문제
* 포스트 코로나 상황에서 항공사에서 고객의 만족도를 위해 대비할 요인들 분석
## 데이터의 구성
* Feauture : ID, Gender, CustomerType, Age, Type of Travel, Class, Flight-Distance, Inflight Wifi Service, Departure/Arrival time convenient,Ease of Online booking,Gate location, Food and drink, Online boarding, Seat comfort, Inflight entertainment, On-board service, Leg room service, Baggage handling, Checkin service, Inflight Service, Cleanliness, Departure Delay in Minutes, Arrival Delay in Minutes
* Target : satisfaction
## Feature Engineering
* 복잡하고 분산이 높은 feature들의 data를 정리해서 새로운 feature로 EDA
* 모델링에 모든 feature를 사용하는 것이 아닌 만족도에 영향을 줄 요인들을 선별 후 사용
## Machine-Learning 모델
* Baseline model : Majority > 빈도수
* Logistic Regression
* DecisionTree classifier
* RandomForest classifier (앙상블)
* Xgboost (앙상블)
## 3K-fold Cross-validation
* 검증정확도가 상위였던 2개의 앙상블 모델을 선택해서 교차검증 결과 두 모델 모두 roc_auc 점수가 높고 일반화 가능하다.
* 별도의 교차 검증 없이도 8만개의 데이터로 데이터의 크기가 충분하다.
## 모델 해석
* Shap 패키지를 이용한 feature의 영향 분석
![shap](uploads/./img/그림1.PNG)
![shap2](uploads/./img/그림2.PNG)
