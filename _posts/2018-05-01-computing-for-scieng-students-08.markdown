---
layout: post
title:  "이공계 대학생/대학원생을 위한 컴퓨팅 강좌 8: 코딩용 고정폭 폰트(fixed-width font) 선택하기"
date:   2018-05-01 22:30:00 -0500
published: no
categories: 강좌
---

# 이공계 대학생/대학원생을 위한 컴퓨팅 강좌 8: 코딩용 고정폭 폰트(fixed-width font) 선택하기

안녕하세요 @jwsohn입니다. 이번 포스팅에서는 코딩을 할 때 쓰는 고정폭
폰트(fixed-width font) 선택에 대해 알아보도록 하겠습니다.

## 고정폭 폰트의 필요성

코딩을 할 때는 기본적으로 글자의 가로 폭이 일정한 고정폭 폰트(fixed-width
font)를 씁니다. 그 이유는 아무래도 터미널(terminal)에서 고정폭 폰트로 코딩을
하던 관습의 영향이 크겠습니다만 고정폭 폰트가 들여쓰기(indentation)과 같은
특성을 가진 소스 코드의 가독성을 높여준다는 이유도 있겠습니다.

그리고 코딩용 폰트는 1, i, l, | 이나 o, O, 0, @ 등과 같이 비슷하게 생긴
영문자, 숫자, 특수기호의 구분을 명확히 해야 하는 특성이 있습니다. 이것은
코딩을 할 때 한 글자만 틀려도 결과가 다르게 나오는 코딩의 특성 때문입니다.
실제 제 경우 학부시절에 `for (j = i + 1; j < n; ++j)`를 `for (j = 1 + 1; j <
n; ++j)`로 잘못 적었다가 i와 1을 구분못해 디버깅에 일주일 가까이를 날려 버렸던
경험이 있습니다.

### 고정폭 폰트의 대표적 예: Courier 

![Courier New](/assets/2018-05-01-computing-for-scieng-students-08/courier-new.png)

윈도우 운영체제에서 기본으로 제공되는 코딩용 고정폭 폰트는 Courier 폰트가
있습니다. (Courier, Courier new) 타자기(typewriter)에 대표적으로 쓰이는
폰트입니다. 

하지만 아쉽게도 Courier 폰트의 컴퓨터 화면 가독성은 그다지 좋지 않습니다.
그래서 코딩용으로는 Courier외에 다른 폰트들이 많이 쓰이는 편입니다.

## 고정폭 폰트 소개

그렇다면 Courier 이외의 가독성이 좋은 고정폭 폰트는 어떤 것이 있을까요? 여러가지
폰트 중에서 일단 무료, 혹은 상용이지만 쉽게 구할 수 있는 폰트를 우선적으로
알아보도록 하겠습니다.

### Dejavu Sans Mono

![Dejavu Sans Mono](/assets/2018-05-01-computing-for-scieng-students-08/dejavu-sans-mono.png)

리눅스 시스템에 거의 기본으로 들어가 있는 고정폭 폰트입니다. 원래는 Bitstream
회사에서 개발한 Vera 폰트를 기반으로 하고 있는데 라이센스가 Bitstream Vera
폰트보다 좀 더 자유롭다고 알려져 있습니다. 

무료로 구할 수 있는 고정폭 폰트 중에서는 거의 최상의 가독성을 갖추고 있고,
유니코드까지 지원하는 장점이 있습니다. 

  * URL: https://dejavu-fonts.github.io/
  * Ubuntu에서 설치 방법: `sudo apt install fonts-dejavu`

#### Hack

![Hack](/assets/2018-05-01-computing-for-scieng-students-08/hack.png)

Deajavu Sans Monospace의 변종입니다. 폰트에 큰 차이는 없지만 0이나 , ; 같은
특수문자의 가독성을 높여서 좀 더 코딩에 특화된 폰트입니다. 제 경우 이 폰트를
코딩 주력으로 쓰고 있습니다.

  * URL: https://github.com/source-foundry/Hack
  * Ubuntu에서 설치 방법: `sudo apt install fonts-hack`

### Noto Mono

![Noto Mono](/assets/2018-05-01-computing-for-scieng-students-08/noto-mono.png)

Android 운영체제를 위해 만들어진 Droid, Roboto 폰트 패밀리의 가장 최근
발전형입니다. 역시 무료로 사용 가능합니다. 참고로 Noto 폰트는 구글에서
진행하고 있는 Unicode 전체를 커버하는 폰트 프로젝트의 산물입니다. 안드로이드
스마트폰에서 볼 수 있는 한글 폰트가 Noto CJK (Chinese, Japanese, Korean)
폰트입니다. 

Noto Mono 폰트는 전체적으로 Dejavu Sans Mono와 비슷하게 생겼습니다만 i, l 과
같은 글자들이 다르게 생겼습니다.

  * URL: https://www.google.com/get/noto/
  * Ubuntu에서 설치 방법: `sudo apt install fonts-noto-mono`

### Inconsolata

![Inconsolata](/assets/2018-05-01-computing-for-scieng-students-08/inconsolata.png)

Microsoft의 Office나 Visual Studio 패키지를 설치하면 추가되는 고정폭 폰트가
Consolas 폰트입니다. 그런데 Consolas 폰트는 상용이라 배포가 자유롭지 못한
문제가 있습니다. Inconsolata 폰트는 이름에서 엿볼 수 있듯이 Consolas 폰트의
영향을 받은 무료 폰트로 처음부터 해상도가 높은 화면에서 더 깨끗하게 출력되는
고품질의 코딩용 폰트 개발을 지향했다는 특성이 있습니다. 

  * URL: http://levien.com/type/myfonts/inconsolata.html
  * Ubuntu에서 설치 방법: `sudo apt install fonts-inconsolata`

### Consolas

![Consolas](/assets/2018-05-01-computing-for-scieng-students-08/consolas.png)

Incosolata에서 말씀드렸듯이 Microsoft의 Office나 Visual Studio 패키지를
설치하면 추가되는 가독성이 좋은 고정폭 폰트입니다.

  * URL: https://docs.microsoft.com/en-us/typography/font-list/consolas

### Cousine font

![Consolas](/assets/2018-05-01-computing-for-scieng-students-08/consolas.png)

Chrome OS의 Core 폰트 시리즈에 포함되어 배포되는 고정폭 폰트입니다. Courier
new와의 자간 metric 호환에 신경을 썼다고 합니다. Chromebook을 쓰면 디폴트로
볼 수 있는 폰트가 되겠습니다.

  * URL: https://github.com/powerline/fonts/tree/master/Cousine
  * Ubuntu에서 설치 방법: `sudo apt install fonts-croscore`

## 한글 고정폭 폰트

### D2Coding 폰트 

![D2Coding](/assets/2018-05-01-computing-for-scieng-students-08/d2coding.png)

오랫동안 가독성 좋은 한글 고정폭 폰트 구하기가 참 어려웠는데요. D2Coding
폰트가 나오면서 이 문제가 상당부분 해결된 느낌입니다. 한글 폰트가
나눔바른고딕에 기반하고 있어서 아주 미려하고 가독성 역시 좋습니다.  특히, 영문
폰트도 미려해서 영문 폰트를 주력으로 쓰는 분들에게도 추천할만한 폰트입니다.
개인적으로 적극 추천하고 싶은 폰트입니다. 마침 Ubuntu 18.04 최신버전부터는
패키지로 다운로드 없이 직접 설치가 가능해졌습니다.

  * URL: https://github.com/naver/d2codingfont
  * Ubuntu에서 설치 방법: `sudo apt install font-naver-d2coding`

### 나눔 코딩

![Nanum Gothic Coding](/assets/2018-05-01-computing-for-scieng-students-08/nanum-gothic-coding.png)

D2Coding 폰트가 나오기 전에 많이 쓰였던 한글 고정폭 폰트입니다. 나눔 고딕
코딩도 좋은 폰트이지만 전체적으로 서체가 너무 가늘고 고해상도 화면에서는
D2Coding이 더 나은 출력 품질을 보여 줍니다. 

  * URL: https://github.com/naver/nanumfont/blob/master/README.md
  * Ubuntu에서 설치 방법: `sudo apt install font-nanum-coding`

## 고정폭 폰트 소개를 마치면서

지금까지 코딩에 적합한 가독성 좋은 고정폭 폰트에 대해 알아보았습니다.
개인적으로 볼 때 전체적으로 Dejavu Sans Mono 계열 폰트들이 가독성이 좋고
무난한 느낌이며 한글 고정폭 폰트로는 D2Coding 폰트가 상당히 뛰어나다고
생각합니다.

폰트 선택은 주관적인 취향이 작용하기 때문에 위에 열거한 폰트 이외에도
다른 선택을 하셔도 좋겠습니다. 다만, 코딩을 할 때에는 고정폭 폰트가 아닌
일반 가변폭 폰트 (variable-width font)를 쓰지는 마시기를 부탁드립니다. 


