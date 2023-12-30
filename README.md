# **서울시 교총 혼잡 요인 분석

**🗓프로젝트 진행 기간:**
2023. 11 ~ 2023. 11

**🏆성과:**
전공 인공지능에서 A+의 성적을 거둠.

**👩🏻‍💻나의 역할:**
    
    
     [Data Analyst]
    
       - 공공 데이터 포털에서 관련 데이터 수집 및 가공
    
       - 데이터 전처리: 주차장 혼잡도
       
       - 주차장 혼잡도 시각화
       
       - 데이터 관계 시각화
       
       - 데이터 분석: 변수 선택(후진 선택법) 및 중회귀 분석 
    

## :bookmark_tabs: 프로젝트 개요
서울시 교통 혼잡도에 영향을 미치는 요인 분석
<br><br>
📌 **'I’m 示'** 는  취향 분석 테스트를 통해 회원 개인의 취향을 분석하고, 회원을 카테고리 별로 분류하여 해당 카테고리에 걸맞은 전시회 정보를 회원에게 제공하는 웹이다. 더 나아가 다양한 전시회를 필터별(인기순, 최신순 등)로 정렬한다. <br><br>


## :bookmark_tabs: 프로젝트 배경

사용자의 취향별 전시회 정보 소개 웹페이지로, 현존해 있는 전시회 정보 사이트들은 대부분 단순히 전시회들의 정보를 소개하여 사용자가 관련 전시회에 대한 정보를 파악하고 있어야 하는 페이지들이 대부분이다. 연령층에 구애 없이 전시회를 관람하는 사람들이 증가하고 있지만, 전시 회에 대해 접한 지 얼마 되지 않은 사용자들 또한 증가하고 있어, 자신이 원하는 종류의 전시회 를 찾기에서 어려움을 겪는다. 이러한 문제들을 해결하기 위해 회원가입 시, 사용자들에게 질문과 그림들을 통해 각 사용자의 취향을 분석하고 저장하여 원하는 전시회를 소개할 수 있도록 한다. 이 웹페이지를 통하여 전시회를 자주 방문하는 사람들은 더 쉽게 전시회를 찾을 수 있을 뿐만 아 니라 전시회를 자주 접해보지 않아서 선택에 어려움을 겪는 사용자들까지 쉽게 원하는 전시회를 찾을 수 있게 된다. 또한 원하는 전시회를 클릭하면 전시회의 위치, 가격, 관련 링크 등을 통하여 정보들을 얻고 북마크를 통하여 더 많은 사람이 문화생활을 좀 더 다양하고 편하게 즐길 수 있음을 기대할 수 있다.
<br>
## :bookmark_tabs: 프로젝트 구성도
<div align="center">
<img width="794" alt="스크린샷 2023-12-07 오전 3 33 05" src="https://github.com/kjw4420/exhibition_platform/assets/97749184/9ebb0119-e327-49b5-adb1-5806b405e816">
</div>

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

### 디자인

조서현

## :hammer_and_wrench: 사용 기술

### Front-end

**프로그래밍 언어**<br>
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white"/> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/> <img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=Javascript&logoColor=white"/>
<br>


### Back-end

**언어**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/> <img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=Javascript&logoColor=white"/><br><br>
**프레임워크/라이브러리**<br>
<img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white"/> <br>

**데이터베이스**<br>
<img src="https://img.shields.io/badge/mysql-4479A1?style=flat-square&logo=mysql&logoColor=white">


