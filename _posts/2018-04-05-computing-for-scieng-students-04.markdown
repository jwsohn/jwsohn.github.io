---
layout: post
title:  "이공계 대학생/대학원생을 위한 컴퓨팅 강좌 4: 이공계 문서 작성의
필수 도구 - LaTeX에 대해 알아보자"
date:   2018-04-05 22:30:00 -0500
published: yes
categories: 강좌
---

# 이공계 대학생/대학원생을 위한 컴퓨팅 강좌 4: 이공계 문서 작성의 필수 도구 - LaTeX에 대해 알아보자

안녕하세요. @jwsohn입니다. 오늘 포스팅에서는 수식이 많고 논리적인 짜임새가
필요한 이공계 문서 작성의 필수 도구인 LaTeX을 쓰는 방법에 대해 간단히
알아보도록 하겠습니다. 참고로, LaTeX은 스티미언들에게 익숙한
마크다운(Markdown)과 비슷한 문법을 쓰기 때문에 스티미언들은 더 친숙하게 배울
수 있는 장점이 있습니다.


## LaTeX이란?

### LaTeX과 Markdown의 간단한 비교

문서의 글제목 (Heading) 넣기를 비교해보겠습니다. 아주 비슷하죠?

|  글제목        | Markdown          | LaTeX                     |
|----------------|-------------------|---------------------------|
|  Heading 1     |`# Heading 1`      |`\section{Heading 1}`      |
|  Heading 2     |`## Heading 2`     |`\subsection{Heading 2}`   |
|  Heading 3     |`### Heading 3`    |`\subsubsection{Heading 3}`|
|  Heading 4     |`#### Heading 4`   |`\paragraph{Heading 4}`    |
|  Heading 5     |`##### Heading 5`  |`\subparagraph{Heading 5}` |

리스트는 이렇게 만듭니다. 우선 Markdown부터 봅시다.

```markdown
List Example
  * one
  * two
  * three
```

LaTeX은 이렇습니다.

```latex
\begin{itemize}
    \item one
    \item two
    \item three
\end{itemize}
```

## LaTeX으로 문서 작성하기

지금까지 예를 보면 LaTeX이나 Markdown 모두 **문서에 명령어를
추가(markup)**해서 글자 모양이나 문서 포맷을 지정하는 것을 알 수 있습니다.
LaTeX의 경우, 명령어는 \로 시작을 하고 추가적인 명령은 {} 사이에 넣는 것을 알
수 있습니다. 그러면, 저번 포스팅에서 간단히 언급했던 Hello, World! 문서
만들기로 다시 돌아가 보겠습니다.

### Hello, World!

```latex
\documentclass{article}

\begin{document}
Hello, World!
\end{document}
```

### Headings

여기에 위에서 배운 글제목을 넣어 보겠습니다. 추가로 문서 제목과 작성일, 글쓴이
이름도 넣어보지요. 소스 코드(source code)를 읽기 편하게 들여
쓰기(indentation)를 넣어 봤습니다. 이 파일을 `hello.tex` 이름으로 저장해
주세요.

```latex
\documentclass{article}    

\begin{document}           

    \title{Hello, world. Welcome to \LaTeX!}          
    \author{jwsohn}        
    \date{April 2018}      

    \maketitle             

    \section{Introduction} 
    This is introduction.  

    \section{Literature Review}                       
    Literatures go here.   

    \section{Experiment}   

        \subsection{Model} 
        Your fine model.   

        \subsection{Experimental Design}              
        Experimental design is important.             

        \subsection{Result}
        Your awesome results.                         

    \section{Discussion}   
    Discuss your results.

    \section{Conclusion}
    Final conclusive remarks.

\end{document}
```

`pdflatex hello.tex` 명령어로 컴파일을 하면 다음과 같은 pdf 파일이 기본으로
생성됩니다.

![hello.pdf](/assets/2018-04-08-computing-for-scieng-students-04/hello-capture.png)

### 문서 기본 템플릿 (template)

LaTeX은 구조적인 글쓰기를 강제(?)하는 특성이 있습니다. 그러니까 문서의
템플릿(template)의 구조에 맞추어 쓸 수 있는 명령어에 차이가 조금씩 있습니다.
또, 폰트를 바꾼다든가, 특정 문단에 다른 스타일을 적용한다든가 하는 작업이
의외로 어렵습니다.

이는 LaTeX이 마이크로소프트 워드(Microsoft Word)와 같은 워드 프로세서의
글쓰기와는 처음부터 지향점부터 다르기 때문인데요, 처음에는 내 마음대로 문서
스타일을 바꾸는 것이 잘 적응이 되지 않겠지만 조금만 적응을 하고 나면
편리해집니다. 

간단한 예로 여러분들이 지금 쓰고 있는 Markdown도 마찬가지입니다. 처음에는 `#`,
`##`, `###` 같은 Heading 명령보다 여러분들의 취향에 맞는 폰트와 폰트 크기를
강제하고 싶으시겠지만 일단 적응이 되고 나면 이것이 좀 더 정돈된 글쓰기에
도움이 되는 것을 알게 되는 것과 마찬가지입니다.

그러면 LaTeX에서 기본으로 제공되는 템플릿은 무엇이 있을까요? 템플릿을 지정하는
`\documentclass` 명령에 article 이외에 다른 형식을 써 볼 수 있겠습니다.
article이외에는 book, report, letter 등등을 쓰실 수 있는데요. 한번 재미삼아
논문 스타일을 써 볼까요? `\documentclass{IEEEtran}`을 쓰면 다음과 같은 pdf
출력이 나옵니다.

![hello-ieeetran.pdf](/assets/2018-04-08-computing-for-scieng-students-04/hello-ieeetran-capture.png)

다음에는 글 전체의 폰트를 바꾸어 보겠습니다. LaTeX에서 기본으로 지원하는
폰트는 Computer Modern이라는 폰트인데 실제 출력을 해 보면 가독성이나 미적인
측면에서 상당한 품질의 폰트임을 알 수 있습니다. 하지만 이 폰트만 쓰려면 좀
지루하겠지요?

문서 전체의 폰트를 바꾸는 것은 `\usepackage`명령을 사용합니다. 폰트 이외에
다른 패키지도 많이 있는데요. (대표적인 것이 그림 넣기 관련 추가 기능을
제공하는 `graphicx` 패키지 같은 것들입니다) 우선은 폰트만 한번 바꾸어 보겠습니다.
여러분들에게 친숙한 Times 폰트를 한번 써 볼까요? `\usepackage{times}` 명령을
아래와 같이 넣어 줍니다. `charter`, `bookman` 같은 폰트도 넣어서 컴파일 해 보세요.
최근에는 안드로이드 스마트폰에서 많이 쓰이는 `droid` 폰트 같은 것들도
지원됩니다.

```latex
\documentclass{article}    

\usepackage{times}

\begin{document}

(이하 생략)
```
![hello-times.pdf](/assets/2018-04-08-computing-for-scieng-students-04/hello-times-capture.png)

LaTeX에서 기본으로 주는 여백이 너무 넓은 것 같은가요? `\usepackage{fullpage}`
명령을 추가하면 되겠습니다.

```latex
\documentclass{article}    

\usepackage{times}
\usepackage{fullpage}

\begin{document}

(이하 생략)
```

이런 식으로 LaTeX에서는 문서의 스타일을 내 마음대로 수정하기보다는 이미
만들어진 문서 템플릿을 가져오고 추가로 패키지를 써서 문서의 모양을 수정하는
쪽으로 나의 문서 작성 방법을 바꾸는 것이 좋겠습니다.

이런 방식이 어떨 때 효과가 있을까요? 네. 여러 명이 모여서 책 같은 긴 문서를
집필할 때 큰 효과를 발휘합니다. 워드 프로세서를 쓰면 아무리 공통된 스타일을
만들고 템플릿 파일을 배포해봐도 사람마다 제각각의 폰트와 문단 정렬을 쓰기가
일쑤입니다. 나중에 부분부분 파일을 모아서 하나로 만들려면 폰트와 문단 정렬만
고치는 것도 큰 일이 되지요. 하지만 LaTeX을 쓰면 애초에 이렇게 하는 것이
어렵습니다.

전체적으로 줄여보면 LaTeX은 글쓰기의 기본에 집중할 수 있는 환경을 만들어 주는
장점이 크다고 할 수 있겠습니다. 여러분들이 여기 스팀잇에서 쓰시는 Markdown도
마찬가지 특성을 갖고 있다고 하겠습니다. 

### 수식 작성

말씀드렸듯이 LaTeX은 수식 작성이 아주 뛰어납니다. 수식 명령어로 수식을 조판해
내는데요. 아래아 한글이나 최근의 마이크로소프트 워드에서 지원하는 수식 명령이
바로 LaTeX에서 기원한 명령들입니다. 수식은 간단히 예를 몇가지 보겠습니다.

```latex
\begin{equation}
    a^2 + b^2 = c^2
\end{equation}

\begin{equation}
    \sum_{i=1}^{n} i = \frac{1}{2} n (n + 1)
\end{equation}

\begin{equation}
    x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\end{equation}

\begin{equation}
    \int f'(x)g(x) dx = f(x)g(x) - \int f(x)g'(x) dx
\end{equation}
```

LaTeX으로 컴파일 하면 다음과 같이 출력됩니다. 수식에 기본으로 (1), (2), (3),
(4)와 같이 수식 번호가 자동으로 붙음을 볼 수 있습니다. 이 역시 나중에 한번 쓴
수식을 `\label` 명령을 이용해 다시 언급할 때 편리합니다. 물론, 수식 번호를
생략하는 명령어 옵션도 있겠습니다. 참고로 수식 외에도 그림(figure),
표(table)와 같은 항목에도 번호가 자동으로 붙습니다.

![Equations](/assets/2018-04-08-computing-for-scieng-students-04/equations-capture.png)

### Reference (BibTeX)

LaTeX의 또 하나의 장점 중 하나는 참고 문헌 (References) 관리입니다. LaTeX
자체에서 참고 문헌을 관리할 수도 있지만 가능하다면 BibTeX이라는 추가 도구를
사용하기를 권장합니다. 특히, 논문을 써야 하는 대학원생의 경우 BibTeX을
사용해서 자신이 갖고 있는 논문 리스트를 만드는 것이 논문을 쓸 때 많은 도움이
됩니다.  BibTeX에서 인용만 하면 자동으로 References 섹션에 지정된 인용
스타일에 맞추어 참고 문헌들이 자동으로 들어가게 됩니다.

BibTeX으로 자신의 논문 리스트를 만드는 것은 비유하자면 자신의 mp3 컬렉션을
관리하는 것과 비슷합니다. 하드 디스크에 저장되어 있는 mp3 파일들을
아이튠즈(iTunes)나 다른 mp3 관리 프로그램을 이용해서 정리하는 것이죠.  이렇게
내 mp3 컬렉션이 관리 프로그램을 통해 정리가 되면 나중에 듣고 싶은 mp3를 찾아
오기가 편리합니다. 아무리 mp3 파일들이 디렉토리나 폴더에 잘 정리되어 있다고
하더라도 말이죠.

논문도 마찬가지입니다. 연구나 공부를 하다보면 내 일과 관련된 논문들이 나오게
되는데요. 좋아하는 mp3를 만날 때마다 mp3 관리 프로그램을 통해 mp3를 등록해
두듯이 중요한 논문을 만나면 논문 관리 프로그램인 BibTeX을 통해서 논문 정보를
등록해 놓을 필요가 있는 것이죠. 참고로 마이크로소프트 워드 환경에서는 상용인
EndNote 프로그램이 유명합니다.

일단 BibTeX의 논문 정보 형식을 한번 볼까요? 이런 엔트리들을 모아 예를 들어
`my-readings-collection.bib` 파일에 저장해 두면 되겠습니다.

```BibTeX
@ARTICLE{gode-sunder-1993,
  author = {Gode, Dhananjay K. and Sunder, Shyam},
  title = {Allocative Efficiency of Markets with Zero-Intelligence Traders:
    Market as a Partial Substitute for Individual Rationality},
  journal = {Journal of Political Economy},
  year = {1994},
  volume = {101},
  pages = {119--137}, 
  number = {1},
  month = feb,
  issn = {0022--3808},
  shorttitle = {Allocative Efficiency of Markets with Zero-Intelligence
Traders},
  abstract = {},
  url = {http://www.jstor.org/stable/2138676}
}
```

BibTeX 논문 정보는 굳이 하나하나 손으로 다 쳐서 만들 필요는 없습니다. 요즘은
왠만한 학술 데이터베이스들이 BibTeX 포맷을 지원하니까요. 한번 Google
Scholar에서 저 논문을 찾아봅시다.

![Google Scholar](/assets/2018-04-08-computing-for-scieng-students-04/gode-sunder-1993.png)

여기서 따옴표 인용 아이콘을 클릭하면 다음과 같은 참고 문헌 정보가 나옵니다.
여기서 BibTeX 링크를 다시 클릭해 보겠습니다.

![Citation](/assets/2018-04-08-computing-for-scieng-students-04/cite.png)

Google Scholar가 생성해 준 이 논문의 BibTeX 정보입니다. 위의 제가 갖고 있는 BibTeX 
논문 정보와는 조금 다르긴 해도 대동소이(大同小異) 함을 볼 수 있습니다. 이렇게 학술
데이터베이스들에서 만들어 주는 BibTeX 데이터를 자신에 필요에 맞게 조금씩 고쳐서
쓰시면 되겠습니다.

```BibTeX
@article{gode1993allocative,
  title={Allocative efficiency of markets with zero-intelligence traders:
Market as a partial substitute for individual rationality},
  author={Gode, Dhananjay K and Sunder, Shyam},
  journal={Journal of political economy},
  volume={101},
  number={1},
  pages={119--137},
  year={1993},
  publisher={The University of Chicago Press}
}
```

BibTeX의 구체적 사용 방법은 초심자 이상의 수준이라 이 포스팅에서는 더
언급하지는 않겠습니다. 다만, 참고 문헌 관리 및 인용에 BibTeX이 유용하게
쓰인다는 점은 꼭 기억해 두시기를 부탁드리겠습니다.

## LaTeX 관련 정보

자, 지금까지 이공계 문서 작성 도구로 중요한 위치를 차지하고 있는 LaTeX을
개괄적으로 알아보았습니다. LaTeX은 간단한 수준으로 배울 수도 있지만 실제
쓰다보면 참고할 만한 자료가 필요합니다. 몇 가지 제 개인적으로 추천 자료를
열거해 보겠습니다.

### WikiBooks: LaTeX (https://en.wikibooks.org/wiki/LaTeX)

WikiBooks의 무료 문서입니다. 여러 가지 예가 설명과 함께 잘 요약되어 있습니다.

### The Not So Short Introduction To LaTeX (https://tobi.oetiker.ch/lshort/lshort.pdf)

역시 무료 문서입니다. 제 개인적으로 WikiBooks: LaTeX과 함께 많이 참조했던
가이드입니다.

### Math Into LaTeX (http://mirrors.ibiblio.org/CTAN/info/mil/mil.pdf)

자세한 설명이 필요한 분들에게 추천하는 책입니다. LaTeX의 세세한 부분까지 잘
설명되어 있습니다. Chapter 1은 무료로 공개되어 있고 나머지 부분은 
필요하시면 책을 구입해 읽으시면 되겠습니다.

### ShareLaTeX (https://www.sharelatex.com)

온라인 LaTeX 에디터 및 컴파일 서비스입니다. 굳이 리눅스 환경이나 다른 곳에서
설치를 하지 않고도 웹 브라우저만을 이용해서 LaTeX을 쓸 수 있게 해 줍니다.
상당히 잘 만들어진 서비스이구요. 추가로 돈을 지불하면 Dropbox 같은 클라우드
저장 서비스와 연동도 가능합니다. 여러가지 문서 템플릿이 많은 것도 장점이고
기본 제공되는 LaTeX 가이드 문서도 잘 쓰여져 있습니다.

### 한국 TeX 사용자 그룹 (http://www.ktug.org)

한국의 TeX 사용자 그룹입니다. 한글로 된 많은 문서와 한글을 LaTeX에서 쓸 때
필요한 것들에 대한 정보가 잘 정리되어 있습니다. 

## 마치며
 
오늘 포스팅에서는 문서 조판 시스템인 LaTeX을 쓰는 방법을 간단히
알아보았습니다. 개인적으로 강조하고 싶은 것은 LaTeX이나 Markdown을 이용한
짜임새 갖춘 글쓰기 습관의 필요성입니다. 글쓰기, 특히 논문과 같은 긴 내용의
글을 쓰는 것은 시간과 노력이 필요한 작업입니다. 이 과정에서 LaTeX과 같은
도구가 짜임새를 갖춘 글쓰기 습관을 기르는데 많은 도움이 됩니다.

그리고, LaTeX의 경우 수식 조판에 뛰어나기 때문에 수식이 많은 이공계 문서
작성에 유용합니다. 아래아 한글이나 마이크로소프트 워드 역시 LaTeX과 비슷한
수식 도구를 제공합니다만 수식이 복잡해지면 수식 렌더링(rendering)에 문제가
생기는 경우가 많습니다. 게다가, 수식의 수가 많아지면 수식을 인용해야 하는데
이럴 때 LaTeX의 수식 인용 기능이 도움이 되겠습니다.

LaTeX은 수식 이외에 그림이나 표, 참고문헌 역시 배치나 인용을 쉽게 할 수 있도록
도와줍니다. 특히, 참고문헌 인용은 BibTeX을 이용하면 편리하고, BibTeX으로 마치
mp3 컬렉션처럼 논문 정보 인덱스를 만들어 놓으면 연구 활동에 많은 도움이
됩니다.

LaTeX을 웹 브라우저에서 편하게 써 보시고 싶은 분들께는 [ShareLaTeX
서비스](https://www.sharelatex.com)를 추천합니다. 

다음 포스팅에서는 프로그래밍으로 주제를 돌아가서 프로그래밍 언어의 최근 추세와
어떻게 프로그래밍 언어를 배우는 것이 좋은지 알아보도록 하겠습니다.

