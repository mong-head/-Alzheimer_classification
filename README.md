# Alzheimer_classification
노인의 데이터로 알츠하이머일지 분별하는 프로젝트

- hands-on-machine-learning 많이 참고

# 1. alzeheimer_all_process.ipynb 

1375명정도의 환자의 데이터를 이용해 알츠하이머일 가능성 예측

* 환자의 데이터 : 70여개의 cortical 두께 정보, 나이 등등

* regression : MMSE, ADAS13 수치를 찾아내는 것. 알츠하이머와 관련있는 수치

* classification : regression한 정보로 3개의 클래스로 나눔. 1단계 : 알츠하이머 걸릴 확률 낮음. 2단계 : 알츠하이머 걸릴 확률 좀 있음. 3단계 : 알츠하이머인 경우


<순서>

1 data 처리 : imputer(median)-scaler(robust) -->pipeline
 - imputer : 없는 값 median으로 채워줌
 - scaler : 범위 벗어나는 값 제외
 
2 regression : rmse와 cross-validation score 비교함, linear,decision tree, randomforest 비교 후 randomforest선택

3 classification : svm, softmax, randomforest 비교 후 randomforest 선택

# 2. alzeheimer_NN_vs_randomforest : randomforest vs. neural network

전 파일에서 머신러닝 방법 중 가장 정확도 높게 나왔던 randomforest와 새로 공부한 neural network 사이 비교

regression, classification 둘 다 randomforest가 더 나았다. 

다만, neural network는 층을 깊이 쌓은 deep neural network가 아니었음.
