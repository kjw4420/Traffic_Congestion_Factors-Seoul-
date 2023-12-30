# **서울시 교총 혼잡 요인 분석

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
## :bookmark_tabs: 기능 소개
 ✔️ **회원 전시 취향 분석:** <br>
 -로그인을 하면 취향 분석 테스트를 할 수 있는 링크가 생성되고 이를 통해 로그인한 회원이 선택하는 대답에 따라서 취향(ex, 현대적, 전통적 등)을 분석하여 Exhibition DB에 있는 Accounts Table에 들어있는 키워드로 분류하여 회원정보와 함께 저장한다.<br>
<br>
 ✔️ **전시 키워드 필터 정렬(최신순, 취향별):** <br>
-Exhibition_detail Table로부터 등록된 전시회 리스트를 받아온 후 필터를 사용해 취향별 (키워드), 최신순으로 정렬하고 이를 사용자에게 보여준다.<br>
<br>
 ✔️ **전시 정보 제공:** <br>
-[일반 사용자]: 사용자가 전시회 리스트에서 누른 전시의 상세정보를 보여준다. 상세정보는 전시회 이름, 전시회 상세설명, 장소, 가격, 공식홈페이지 링크, 사진 촬영 가능 여부를 포함한다. <br>
-[관리자]: 전시정보를 등록하는 것으로 전시회 이름, 전시회 상세설명, 장소, 가격, 공식홈페이지 링크, 사진 촬영 가능 여부에 대한 정보를 삽입, 삭제, 갱신(수정)이 가능하도록 한다.<br><br>

<div align="center">
<img width="683" alt="스크린샷 2023-09-12 오전 1 58 12" src="https://github.com/kjw4420/exhibition_platform/assets/97749184/3bf166cf-8f29-40c9-af77-76fcf0767f8a"><br>
<img width="683" alt="스크린샷 2023-09-12 오전 1 58 05" src="https://github.com/kjw4420/exhibition_platform/assets/97749184/87064bbc-0f45-4cd3-9d2f-ca029c936fe2"><br>
<img width="683" alt="스크린샷 2023-09-12 오전 1 58 24" src="https://github.com/kjw4420/exhibition_platform/assets/97749184/47ddc16d-e29e-4f6f-aa94-ca2ceca2942d"><br>
<img width="820" alt="스크린샷 2023-09-12 오전 1 58 41" src="https://github.com/kjw4420/exhibition_platform/assets/97749184/3b540fc5-2575-4e7d-b67c-14b9fa6a8e30"><br>
<img width="820" alt="스크린샷 2023-09-12 오전 1 58 54" src="https://github.com/kjw4420/exhibition_platform/assets/97749184/ab56812d-dbc5-4548-8328-9890e4f9ecda">
</div>

## :bookmark_tabs: 문제해결: 의사결정 && 프론트의 부재
- 의사결정

데이터베이스 설계 과정에서, 팀원과 저는  테이블 구조에대해 서로 다른 의견을 가졌습니다. 어떤 테이블 구조가 최적인지 결정하기 위해서는 서로의 생각을 명확히 이해해야 했습니다. 저희는 각자의 아이디어를 정확하게 전달하기 위해 노력했고, 서로의 의견을 이해하기 위해 칠판에 그림을 그리며 2시간 동안 설명하고 토의했습니다. 이 과정을 거쳐 결국 하나의 테이블 구조를 채택했습니다.

그러나 이 과정에서 전혀 갈등을 일으키지 않았고, 자신만의 의견을 고집하지도 않았습니다. 제 동료는 뛰어난 능력과 배울 점이 많은 사람이라고 믿었기 때문입니다. 이 경험을 통해 앞으로의 협업에서는 서로의 의견을 존중하고 대화를 통해 해결책을 찾는 것이 중요하다는 것을 느꼈습니다. 상대방을 이해하고 합의점을 찾아가며 협력하는 자세가 효과적인 팀워크를 이끌어낼 수 있다는 것을 배웠습니다.

- 프론트의 부재

팀원과 저는 둘 다 백엔드 개발에 익숙하여 화려한 프론트엔드를 구현하는 데 어려움을 겪었습니다. 이를 극복하기 위해 Bootstrap을 활용했습니다.

그러나 세부적인 디테일 부분에서 여전히 프론트엔드의 한계를 느꼈습니다. 이 경험을 통해 HTML/CSS를 더 깊이 공부하고 습득해야겠다는 필요성을 느꼈습니다. 백엔드 능력 외에도 프론트엔드 지식을 확장하여 팀 내에서 더 다양한 역할을 수행하고 협력할 수 있을 것이라고 생각합니다.

## :bookmark_tabs: 키워드 필터링
- 회원가입시 간단한 테스트를 통해 사용자에게 키워드 부여
- 해당 키워드를 가진 전시회 리스트 정렬: 회원별 전시회 추천
- 전체 정보 최신순 정렬

```python
#필터 정렬(최신, 키워드))
def sort(request,key):
    login_session = request.session.get('login_session','')
    if login_session == '':  #로그인 X
        login_session= False
        if key=="최신순": #최신순 정렬
            exhibition= ExhibitionDetail.objects.all().order_by('-exhibition_id') #전시회 정보 테이블로부터 생성 id기준 최신 정렬
            filter=False #sort.html에서 드롭다운을 위한 filter 변수
            return render(request, 'Sort/sort.html', {'exhibition':exhibition, 'key':key,'filter':filter,'login_session':login_session})    
        else: #필터정렬
            exhibition=ExhibitionDetail.objects.filter(keyword=key) #키워드 필터링(user가 가지고 있는 key값 기준)
            exhibition=exhibition.order_by('-exhibition_id') #키워드 필터링 후 키워드 s최신순 정렬
            filter=True #sort.html에서 드롭다운을 위한 filter 변수
            return render(request, 'Sort/sort.html', {'exhibition':exhibition, 'key':key,'filter':filter,'login_session':login_session})    
    else: #로그인 O     
        login_session= True
        id=request.session['login_session']  #현재 admin 로그인 세션 정보 받아오기
        user=Account.objects.get(userid=id) #로그인 한 admin 세션으로부터  admin 객체 상세 정보 받아오기
        keyword=user.keyword #admin user의 id값
        if key=="최신순": #최신순 정렬
            exhibition= ExhibitionDetail.objects.all().order_by('-exhibition_id') #전시회 정보 테이블로부터 생성 id기준 최신 정렬
            filter=True #sort.html에서 드롭다운을 위한 filter 변수
            return render(request, 'Sort/sort.html', {'exhibition':exhibition, 'key':key,'keyword':keyword,'filter':filter,'login_session':login_session}) 
        else: #필터정렬
            exhibition=ExhibitionDetail.objects.filter(keyword=key) #키워드 필터링(user가 가지고 있는 key값 기준)
            exhibition=exhibition.order_by('-exhibition_id') #키워드 필터링 후 키워드 s최신순 정렬
            filter=True #sort.html에서 드롭다운을 위한 filter 변수
            return render(request, 'Sort/sort.html', {'exhibition':exhibition, 'key':key,'keyword':keyword,'filter':filter,'login_session':login_session}) 
```
<div align="center">
sort/views.py
</div>
  


## 👩🏻‍💻 멤버

### Front-end/back-end

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
<img src="https://img.shields.io/badge/Jupyter-#F37626?style=flat-square&logo=mysql&logoColor=white"/>


