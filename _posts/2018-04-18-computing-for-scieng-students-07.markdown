---
layout: post
title:  "이공계 대학생/대학원생을 위한 컴퓨팅 강좌 7: 코딩에 필요한 통계학, 수학, 영어"
date:   2018-04-18 22:30:00 -0500
published: yes
categories: 강좌
---

# 이공계 대학생/대학원생을 위한 컴퓨팅 강좌 7: 코딩에 필요한 통계학, 수학, 영어

안녕하세요 @jwsohn입니다. 이번 포스팅에서는 지금까지 강좌에서 언급되지 못했던
코딩에 도움이 되는 기타 여러가지들을 종합해 보겠습니다. 그런데 이번에는 마침
글을 쓰다보니 여러가지 대학 교재에 대한 추천이 많이 포함되었습니다. 이번 글
구성은 크게 통계학, 수학, 영어 학습 파트로 나누어 보겠습니다.

## 통계학 공부 

인터넷이 일상화되면서 세상이 많이 바뀌었습니다. 이제는 컴퓨터로 개발을 한다는
것이 과거(?)처럼 컴퓨터를 잘 이해하는 것으로 충분하지 않고 사용자의 행동과
특성까지 이해해야 할 필요성이 증대되었습니다. 이런 까닭에 사용자 데이터 분석이
중요해졌는데요.

여기에 소위 빅 데이터라고 불리는 경향은 분석이 필요한 데이터의 사이즈가 너무
커져서 일반적인 통계 기법 만으로는 분석이 쉽지 않아졌다는 점에 주목하고
있습니다. 또한, 데이터의 크기가 커지고 컴퓨팅 파워가 증대되면서 기존에는
유용하지 않았던 기법이 효율이 높아지는 경우도 발생하고 있습니다.

### 통계학 수업

그러면 빅 데이터 처리를 위한 통계 기법을 배우기 위해서는 무엇이 필요할까요?
우선, 기본적으로 고등학교 때 배우는 확률 통계, 특히 조건부 확률은 열심히 해
둡시다. 이게 잘 안되면 아무리 좋은 패키지를 써서 분석을 해도 사상누각이 될
가능성이 높습니다. 기본 가정과 전제를 무시한 채 분석을 하기 쉬우니까요.

고등학교 수준의 확률 통계 기본을 다지고 난 다음 대학 과정에서는 아무래도 선형
회귀분석(linear regression) 수업을 들어야 하겠지요. 이게 되어야 기초적으로
변인(variables)들 간의 상관관계(correlation)와 인과관계(causation)와의 차이를
생각할 수 있게 됩니다. 이 차이점을 훈련 받지 않으면 correlation만 보고
causation이라고 우기는 통계 선무당이 될 가능성이 높아지는 위험성이 항상
따라오게 됩니다.

또, 정규 분포(normal distribution)가 왜 중요한지, 통계학적
모집단(population)과 표본집단(sample)의 차이는 무엇인지, 어떻게 sample을
이용해서 population을 추정(inference)할 수 있는지 훈련이 잘 되어야 합니다. 

그리고, 요즘은 아마도 학부에도 데이터 마이닝(data mining) 수업이 많이 개설되어
있을 것입니다만 data classification이라고 할 수 있는 data mining역시 linear
regression의 연장이자 응용입니다. 크게 data mining은 확률 분포나 가정에 기반한
통계학적 접근과 알고리즘적 기반의 컴퓨터 공학적 접근으로 나누어 볼 수 있는데
통계학적 접근을 이해하기 위해서는 통계학의 이론 이해가 꼭 필요합니다. 즉,
이러기 위해서는 linear regression 과목을 우선 수강한 다음 data mining 수업을
수강하는 것이 필요합니다.

추가로 일반 대학원생들은 통계학과에서 개설하는 대학원 1학년용 (보통 500대
과목이라고 부르는) 통계학 수업을 듣기를 추천해드립니다. 통계는 어느 연구에나
방법론으로 쓰이는 까닭에 연구가 필요한 대학원생들은 전공에 상관없이 통계학을
알아야 하는데요. 이렇게 비전공 대학원생을 대상으로 특별히 개설된 수업들이 이
500대 통계학 수업입니다. 대학원생들 대상 수업이지만 비전공자 대상이라 학부
통계학 수업과 다루는 내용이 큰 차이가 없습니다. 

### Data mining

Data mining은 중요한 교재 둘이 무려 공짜로 공개되어 있습니다. 두 교재 모두
조금 어렵긴 하지만 아마 대부분의 대학에서 이 교재를 쓰고 있지 않을까 싶습니다.
일단 소개를 해 보지요.

#### An Introduction to Statistical Learning

![An Introduction to Statistical Learning](/assets/2018-04-18-computing-for-scieng-students-07/isl-cover.jpg)

An Introduction to Statistical Learning
  * 저자: Gareth James, Daniela Witten, Trevor Hastie and Robert Tibshirani
  * URL: http://www-bcf.usc.edu/~gareth/ISL

학부 3, 4학년과 비전공 대학원 학생들을 위한 교재입니다. 책 제목과는 달리 통계
뿐만 아니고 데이터 마이닝 기법들도 잘 커버하고 있습니다. 챕터마다 Lab
session이 따라오고 R 소스코드가 제공됩니다. 우선 이 책으로 시작을 하시고 더
필요하다면 다음 교재를 보시는 것을 추천합니다.

#### The Elements of Statistical Learning

![The Elements of Statistical Learning](/assets/2018-04-18-computing-for-scieng-students-07/esli-cover.jpg)

The Elements of Statistical Learning
  * 저자: Trevor Hastie, Robert Tibshirani, and Jerome Friedman
  * URL: https://web.stanford.edu/~hastie/ElemStatLearn

데이터 마이닝을 깊이 파야 하는 전공자들이나 대학원 학생들 전용 교재입니다.
700 페이지 갸량의 상당한 분량에서 데이터 마이닝의 중요한 기법들을 잘 커버하고
있습니다. 

## 수학 공부

이렇게 통계학 공부를 하려면 기본적으로 수학 지식이 필요할 겁니다. 통계학의
기본이 되는 수학은 무엇보다 고등학교 수준에서는 행렬(matrix)과 벡터(vector)를
잘 해야 하겠지요. 여기에 추가해서 대학 수준에서는 선형 대수학(linear algera)을
수강해서 행렬을 다루는 실력을 높일 필요가 있겠습니다. 

선형 대수학은 좋은 교재들이 많이 있습니다만 제 개인적으로는 이 교재를
추천합니다. Gilbert Strang의 Introduction to Linear Algebra 입니다.

#### Introduction to Linear Algebra 

![Introduction to Linear Algebra](/assets/2018-04-18-computing-for-scieng-students-07/linear-algebra-strang.jpg)

Introduction to Linear Algebra 
  * 저자: Gilbert Strang
  * URL: http://math.mit.edu/~gs/linearalgebra/

역사와 전통(?)을 자랑하는 교재입니다. 판형을 거듭해서 5판이 나와 있네요. 잠깐
구글 검색을 해 보니까 이전 판본은 pdf 파일 검색도 잘 됩니다. ㅎㅎ

Strang의 홈페이지에 가 보면 교재에서 부분들을 발췌해 두었습니다. 행렬의 소개,
역행렬 연산, Eigenvalue, image processing, 평균 분산 및 확률 등등인데요.
시간이 바쁘신 분들은 발췌본만 잘 읽어보셔도 도움이 되지 않을까 싶습니다.

## 영어 공부 

자꾸 배보다 배꼽이 커지는 느낌입니다. 통계학에서 수학까지, 이제는 영어까지
주제가 넘어가고 있으니까요. 그래도 어쩌겠습니까. 코딩과 관련된 많은 교재와
자료들은 영어로 되어 있는 것을요. 게다가, 기본적인 개발자들의 숫자가 영어권이
한국어권보다 훨씬 많습니다.

개발자를 위한 영어 실력은 어느 정도가 필요할까요? 기본적으로 대학 학부 교재를
읽는데 문제가 없고 인터넷 상의 개발자 포럼의 질문/답변을 이해하는데 문제가 없으면
충분하다고 생각합니다. 즉, 읽기, 혹은 독해가 중요하고 말하기나 듣기는
상대적으로 덜 중요하다는 것이지요.

### 단기간에 독해 실력 늘려보기

영어 공부를 위해서는 어떻게 공부하는 것이 좋을까요? 언어 학습은 장기간 꾸준히
지속하는 것이 최선입니다만 제 개인적인 경험으로는 단기간(?)에도 독해 실력은
올릴 수 있었습니다. 하루 한두시간 정도 해서 대략 3개월 정도면 상당한 차이가
발생합니다.

제가 하던 방법은 이렇습니다. 

  1. 읽을 기사를 하나 고릅니다. 제 경우는 제 영어 선생님의 추천으로
     Reader's digest 잡지 (http://rd.com) 의 기사를 잘 골랐습니다.
     Reader's digets는 다양한 분야에 나오는 책이나 잡지를 정리(digest)해서
     출간하기에 기사 분량도 적당하고 실제 영어권 독자들이 평균적으로 읽는
     글을 접하게 되는 장점이 있습니다.
  2. 고른 기사를 읽습니다. 그리고 모르는 단어를 노트에 정리합니다.
  3. 하루 지나서 새로 나온 단어의 뜻을 체크해봅니다. 그리고 다음 기사로 넘어 갑니다.

이 방법을 계속 반복해서 3개월 정도 하고 나니까 모르는 단어를 사전에서 찾는
일이 많이 줄어들었습니다. 대략 왠만한 단어는 서너번 정도 이렇게 찾고 외우고
까먹고 사이클이 반복되면서 외워지구요. 오래 걸려도 이 사이클이 7번 정도를 넘어
가는 단어는 없었던 것 같습니다. 또한, 중요한 단어일수록 까먹어도 그만큼 자주
다시 나오기 마련입니다.

이런 과정이 반복되면서 웬만한 신문 기사 읽기도 아주 수월해졌구요. 일단 이것을
3개월 정도를 하고 나면 관성이 붙기 때문에 그 다음부터는 꾸준히 계속해도 되고
아니면 공부 빈도를 줄여 나가도 괜찮습니다.

참고로 대학원, 특히 미국 유학을 생각하시는 분들은 GRE 시험 준비에 필요한
고수준(?) 단어를 외울 필요가 있습니다. 소위 GRE 수준 단어들이 큰 쓸모는 없지만
독해를 하면서 편하게 외워 두면 나중에 시험 준비를 할 때 스트레스를 많이 덜 수
있습니다.

GRE 대비용으로 단어 수준을 올리려면 많이 알려져 있는
Time誌(http://time.com) 를 읽으면서 새로 나오는 단어들을 외워 나가면 되구요.
이쪽의 끝판왕은 아무래도 Economist誌(https://www.economist.com) 가 되겠습니다.
Economist는 정말 기사는 잘 쓰는 데 그만큼 읽기도 신경써야 하는 그런 시사 잡지인
것 같습니다. 

### StackExchange 서비스의 코딩 질문/답변

![StackOverflow](/assets/2018-04-18-computing-for-scieng-students-07/stack-overflow.png)

StackExchange (https://stackexchange.com/sites#) 가 있기 전에는 어떻게 코딩을
했을까요? 코딩에 대한 왠만한 질문들은 이미 다 답변이 잘 정리되어 있는 곳이
StackExchange입니다.

특히, 구체적으로 코딩에 관한 질문들은 이곳에서도 StackOverflow.com
(http://stackoverflow.com) 에 올라옵니다. 적당히 키워드만 잘 넣어도 구글이
알아서 StackOverflow.com의 해당 Q&A를 잘 찾아 줍니다. 혹시 잘 안찾아지면
입력할 키워드 다음에 `stackoverflow` 단어만 하나 더 붙이면 웬만한 경우 내가
찾는 질문과 그에 대한 답변이 나옵니다. 

StackOverflow는 프로그래머의 입장에서는 코딩의 방법을 획기적으로 변화 시킨
서비스라고 볼 수 있습니다. 코딩을 하면서 만나는 구체적인 문제 하나하나에
대해서 이렇게 잘 정돈되고 검색이 용이한 서비스가 StackOverflow 이전에는
없었으니까요. 그만큼 코딩을 하면서 실제 만나는 문제를 푸는데 실용적인 서비스가
StackOverflow가 되겠습니다.

### Safari at O'Reilly

![Safari at O'Reilly](/assets/2018-04-18-computing-for-scieng-students-07/safari-oreilly.png)

그렇다고 질문/답변 검색만으로 코딩의 문제가 해결되지는 않지요. 기본 실력을
다져주는 Technical books의 대표격인 출판사가 O'Relly (http://oreilly.com)
인데요. 이 출판사의 소위 동물 시리즈(animal series) 책들은 좋은 내용과
구성으로 프로그래머들에게 많은 도움이 됩니다. 여기서 책에 동물 시리즈라는
별칭이 붙은 이유는 항상 책 표지에 동물 그림을 넣기 때문입니다.

Safari (https://www.safaribooksonline.com) 는 온라인으로 O'Reilly의
모든 동물 시리즈 책들을 열람할 수 있게 해 주는 서비스입니다. 동물 책들이 모여
있으니 사파리 동물원이 된다는 재미있는 작명(作名)인데요. 문제는 이 서비스가 좀
비싼 편입니다. 개인이 쓰기에는 부담스러운 측면이 있습니다.

그런데 Safari는 상당수의 대학 도서관에서 무료로 서비스를 하는 경우가 많습니다.
보통, 대학의 아이피 주소에서 접속하거나 대학 컴퓨터 계정이 있으면 Safari까지
무료로 억세스 할 수 있게 해 주는 형태로 무료 서비스가 제공됩니다. 학생들이면
다니고 있는 학교의 도서관 서비스에 Safari가 포함되어 있는지 꼭 확인해 보시기
바랍니다. 

## 마치면서

지금까지 코딩에 도움이 되는 기타 여러가지에 대해 알아보았습니다. 전체적으로
쓰고 나서 보니 대학 교재 추천과 영어 공부 방법 추천이 되고 말았습니다. 

제 개인적으로는 일찍 중고등학교 때 영어 수학의 기본을 잘 배우는 행운을 얻어서
대학 이후의 상대적으로 적은 노력에도 코딩을 하는데 영어 수학 관련해서는
어려움을 겪지 않고 있습니다. 하지만 통계의 경우는 과거 그 당시 중요성을 몰라서
잘 안배웠기 때문에 지금도 따라가는데 어려움을 느끼고 있습니다. 특히, data
mining에서 최근의 deep learning으로 넘어간 최신 경향은 바쁘다는 핑계로 배우는
것을 차일피일 미루고 있는 상황입니다.

어쨌든, 코딩을 하면서 기본이 되는 통계, 수학, 영어 실력은 반드시 필요하다고
봅니다. 특히, 빅 데이터 이후로 통계학의 필요성이 최근들어서는 계속 증대되고
있는 추세입니다. 기회가 되시는 학생 여러분들이 이 세 가지 기초를 잘 다졌으면
하는 희망을 이 글을 쓰면서 해 봅니다. 


