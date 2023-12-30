# **서울시 교통 혼잡 요인 분석**

**🗓프로젝트 진행 기간:**
2023. 11 ~ 2023. 11

**🏆성과:**
전공 인공지능에서 A+의 성적을 거둠.

**👩🏻‍💻나의 역할:**
    
    
     [Data analysis]
    
       - 공공 데이터 포털에서 관련 데이터 수집 및 가공
    
       - 데이터 전처리: 주차장 혼잡도
       
       - 주차장 혼잡도 시각화
       
       - 데이터 관계 시각화
       
       - 데이터 분석: 변수 선택(후진 선택법) 및 중회귀 분석 
    

## :bookmark_tabs: 프로젝트 개요
**목적:** 서울시 교통 혼잡도에 영향을 미치는 요인 분석<br>
**데이터:** 모든 데이터는 공공데이터포털 한국교통연구원 2022년 행정구역단위 교통 데이터를 이용했으며, 데이터를 자치구 기준으로 유의미 하다고 추측되는 데이터들을 가공 및 추가했습니다
<br><br>

## :bookmark_tabs: 데이터 살펴보기
분석할 데이터의 열, 개수, 데이터 타입을 확인한다.
<div align="center">
<img width="876" alt="데이터살펴보기" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/4991aae5-d606-42fd-8270-1c85da1126a6">
</div>
<br>

## :bookmark_tabs: 데이터 전처리
- 전체 추정 교통량
    - 관측교통량과 내비게이션 데이터를 이용하여 미관측 도로의 교통량을 추정하는 알고리즘을 통해 추정된 교통량. 도로를 주행하는 차량의 수를 의미하며, 읍면동 경계로 구분된 데이터로 단위는 대/일
    - 전체추정교통량은 승용차추정교통량, 버스추정교통량과 화물차추정교통량의 합산치
<div align="center">
<img width="892" alt="전체추정교통량" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/8a8f5e4f-84b3-41b8-b8cd-86b70f9df9e2">
</div><br>

- 혼잡시간강도
    - 도로를 주행하는 모든 차량이 경험한 총 통행시간대비 혼잡을 경험한 차량의 총 통행시간의 비율을 의미, 읍면동 경계로 구분된 데이터로 단위는 %
    - 혼잡의 정도를 시간을 중점으로 나타낸 특성
<div align="center">
<img width="740" alt="혼잡시간강도" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/eb8bd50b-f08a-4591-b090-53b231f8b85d">
</div><br>

- 혼잡빈도강도
    - 혼잡빈도강도는도로를주행하는모든차량대수중혼잡을경험한차량대수비율을의미 읍면동 경계로 구분된 데이터로 단위는 %
    - 혼잡의 정도를 차량의 대수를 중점으로 나타낸 특성
<div align="center">
<img width="740" alt="혼잡빈도강도" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/0483db0c-975a-44ff-a0b8-2733807edbe1">
</div><br>

- 등록차수 & 교통량
    - 등록차수는 행정구역단위의 2022년 한 해 동안 등록된 자동차의 수
    - 왼쪽 데이터에서 행정구역단위 모든 유형의 자동차 등록수를 모두 합해 오른쪽 데이터의 등록차수로 표현
    - 교통량은 등록차수에서 파생된 데이터로 전체추정교통량대비 등록차수의 비율
 <div align="center">
<img width="1179" alt="등록차수_교통량" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/5b7cf738-d684-4d4f-a481-e48db36dd075">
</div><br>

- 주차장 혼잡평균
    - 주차장혼잡평균은 서울시 행정동별 시간별 주차현황의 1년치 데이터에서 주차장에따라 동일 시간대 시간당입구출입의 평균치에서 파생된 데이터
    - 데이터를 살펴보면 대부분 아침 08, 09, 10시와 저녁 18, 19, 20시의 입구 출입이 가장 많은 것을 알 수 있다. 따라서 본 프로젝트의  목표는 교통 혼잡도에 영향을 미치는 요인 분석이므로 해당 데이터에서 가장 혼잡 시간인 아침 08, 09, 10시 저녁 18, 19, 20시의 평균치를 나타냈다.
     <div align="center">
<img width="1239" alt="주차장1" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/bb2e5455-bfc2-4ba8-b3ac-3f650da9f411">
<img width="1292" alt="주차장2" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/fa117e7a-33d1-4d29-beed-e8894cd5c0a3">
</div> <br><br>

## :bookmark_tabs: 피어슨 상관계수
- 혼잡시간강도, 혼잡빈도강도를 중심으로 데이터를 살펴보자.
    - 혼잡시간강도와 혼잡빈도강도: 0.94로 강한 양의 상관관계
    - 혼잡시간강도: 승용차추정교통량, 버스추정교통량이 약한 양의 상관관계, 교통량이 약한 음의 상관관계
    - 혼잡빈도강도: 전체추정교통량, 등록차수, 승용차추정교통량, 버스추정교통량이 약한 양의 상관관계, 교통량 약한 음의 상관관계
- 전체추정교통량은 승용차추정교통량, 버스추정교통량, 화물차추정교통량의 합산치이므로 이들 간 강한 양의 상관관계
- 예상외로 주차장혼잡평균은 해당 분석에서 미비한 영향을 끼치는 것으로 보여진다.
   <div align="center">
<img width="723" alt="피어슨" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/0a415983-9b54-400b-8693-b9fe6e2dfdd8">
</div> <br><br>

## :bookmark_tabs: 변수 선택법: 후진 선택법
- 종속변수(Y): 혼잡시간강도
- 독립변수(X): 혼잡빈도강도, 전체추정교통량, 등록차수, 교통량, 승용차추정교통량, 버스추정교통량, 화물차추정교통량, 주차장혼잡평균
- 변수 선택 결과: 혼잡빈도강도, 버스추정교통량
 <div align="center">
<img width="604" alt="변수선택" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/2a40baa8-45cd-43e9-9192-1b50f38642aa">
</div> <br><br>

## :bookmark_tabs: 중회귀 분석 및 결과
- 종속변수(Y): 혼잡**시간**강도
- 분석 참여 변수(X): 혼잡빈도강도, 버스추정교통량
- 분석 결과:
    - R-Squared 값은 약 88%로 높은 설명력을 가지며, F통계량이 충분히 낮은 유의확률을 가지고 있어 모델이 유의미하다고 판단.
    - 모든 독립변수의 P-value가 0.05보다 낮아 두 변수 모두 종속변수 혼잡시간강도에 영향을 미친다.
    - 잔차분포를 살펴보면, 왜도(skew)는 -0.486으로 0에 충분히 가깝고, 첨도(kurtosis)는 뾰족하지만 3에 가까우므로 잔차가 정규분포를 따른다.
    - 더빈왓슨 통계량은 1.874로 2에 가까운 값이므로 잔차간 자기 상관성 또한 적절하다.
    - 다중공선성은 831로 충분히 작은 값이므로 예측력 좋다.
- 결과적으로, 혼잡시간강도를 예측하는 데에 버스추정교통량과 혼잡빈도강도는 영향을 미치는 유의미한 변수이며, 이 모델은 데이터를 잘 설명하고 있는 것으로 보입니다.
 <div align="center">
<img width="568" alt="분석결과" src="https://github.com/kjw4420/Traffic_Congestion_Factors_in_Seoul/assets/97749184/bb5cee9c-d17c-4388-917f-60c96f5e5dec">
 </div><br><br>


## :bookmark_tabs: 문제해결: 변수선택 단계 추가
다중 공선성 문제를 해결하기 위해 후진 선택법을 활용했습니다. 처음에는 8개의 독립 변수를 이용하여 모델을 구축했지만, 이로 인해 다중 공선성이 높아져 모델의 예측력이 떨어졌습니다. 그래서 후진 선택법을 이용해 유의미한 변수만을 선택하여 최적화된 모델을 구축했고, 이를 통해 독립 변수의 수를 8개에서 2개로 줄여 다중 공선성을 낮추었습니다.

후진 선택법을 사용한 이유는 다른 선택법에 비해 후진 선택법이 독립변수가 많은 전체 데이터에서 다중 공선성을 줄이는 데 효과적이라고 판단했기 때문입니다. 이 방법은 모든 변수를 포함한 상태에서 하나씩 제거해 나가는 방식으로, 각 변수가 모델에 미치는 영향을 순차적으로 평가하면서 가장 중요한 변수들을 선별합니다. 이를 통해 모델의 복잡성을 줄이고 예측력을 향상시킬 수 있었습니다. 이러한 전략 선택과정을 통해 데이터 분석에서 모델의 정확성을 향상시키는 중요한 전략을 경험하고 익힐 수 있었습니다.<br><br>


## 👩🏻‍💻 멤버

### Data Analysis

|               | github                             |
| ------------- | ---------------------------------- |
| 김지원  |https://github.com/kjw4420    |
| 조서현        |   https://github.com/westnowise      |



## :hammer_and_wrench: 사용 기술



### Back-end

**언어**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/> 
**프레임워크/라이브러리**<br>
<img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white"/> <br>

**데이터베이스**<br>
<img src="https://img.shields.io/badge/Jupyternotebook-#F37626?style=flat-square&logo=mysql&logoColor=white"/>


