---
layout: post
title:  "이공계 대학생/대학원생을 위한 컴퓨팅 강좌 4: 이공계 문서 작성의
필수 도구 - LaTeX에 대해 알아보자"
date:   2018-03-28 22:30:00 -0500
published: no
categories: 강좌
---

# 이공계 대학생/대학원생을 위한 컴퓨팅 강좌 4

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
Hello, World
\end{document}
```

### Headings

여기에 위에서 배운 글제목을 넣어 보겠습니다. 추가로 문서 제목과 작성일, 글쓴이
이름도 넣어보지요. 소스 코드(source code)를 읽기 편하게 들여
쓰기(indentation)를 넣어 봤습니다.

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

![hello.pdf][/assets/2018-04-02-computing-for-scieng-students-04/hello-capture.png]

### 문서 기본 템플릿 (template)

LaTeX은 구조적인 글쓰기를 강제(?)하는 특성이 있습니다. 그러니까 문서의
템플릿(template)의 구조에 맞추어 쓸 수 있는 명령어에 차이가 조금씩 있습니다.
또, 폰트를 바꾼다든가, 특정 문단에 다른 스타일을 적용한다든가 하기가 의외로
어렵습니다.

이는 LaTeX이 워드(Microsoft Word)와 같은 워드 프로세서의 글쓰기와는 처음부터
지향점부터 다르기 때문인데요, 처음에는 내 마음대로 문서 스타일을 바꾸는 것이
잘 적응이 되지 않겠지만 조금만 적응을 하고 나면 편리해집니다. 

간단한 예로 여러분들이 지금 쓰고 있는 Markdown도 마찬가지입니다. 처음에는 `#`,
`##`, `###` 같은 Heading 명령보다 여러분들의 취향에 맞는 폰트와 폰트 크기를
강제하고 싶으시겠지만 일단 적응이 되고 나면 이것이 좀 더 정돈된 글쓰기에
도움이 되는 것을 알게 되는 것과 마찬가지입니다.

그러면 LaTeX에서 기본으로 제공되는 템플릿은 무엇이 있을까요? 템플릿을 지정하는
`\documentclass` 명령에 article 이외에 다른 형식을 써 봅니다. article이외에는
book, report, letter 등을 쓰실 수 있는데요. 한번 재미삼아 논문 스타일을 써
볼까요? `\documentclass{IEEEtran}`을 쓰면 다음과 같은 pdf 출력이 나옵니다.

![hello-ieeetran.pdf][/assets/2018-04-02-computing-for-scieng-students-04/hello-ieeetran-capture.png]

다음에는 글 전체의 폰트를 바꾸어 보겠습니다. LaTeX에서 기본으로 지원하는
폰트는 Computer Modern이라는 폰트인데 실제 출력을 해 보면 가독성이나 미적인
측면에서 상당한 품질의 폰트임을 알 수 있습니다. 하지만 이 폰트만 쓰려면 좀
지루하겠지요?

문서 전체의 폰트를 바꾸는 것은 `\usepackage`명령을 사용합니다. 폰트 이외에
다른 패키지도 많이 있는데요. (대표적인 것이 그림 넣기 관련 추가 기능을
제공하는 graphicx 패키지 같은 것들입니다) 우선은 폰트만 한번 바꾸어 보겠습니다.
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
![hello-times.pdf][/assets/2018-04-02-computing-for-scieng-students-04/hello-times-capture.png]

LaTeX에서 기본으로 주는 여백이 너무 넓은 것 같은가요? `\usepackage{fullpage}`
명령을 추가하면 되겠습니다.

```latex
\documentclass{article}    

\usepackage{times}
\usepackage{fullpage}

\begin{document}

(이하 생략)
```

이런 식으로 LaTeX에서는 문서의 스타일을 내 마음대로 수정하기보다는 이미 만들어진 문서
템플릿을 가져와 패키지를 써서 문서의 모양을 수정하는 쪽으로 문서 작성 방법을
바꾸는 것이 좋겠습니다.

이런 방식이 어떨 때 효과가 있을까요? 네. 여러 명이 모여서 책 같은 긴 문서를
집필할 때 효과를 발휘합니다. 워드 프로세서를 쓰면 아무리 공통된 스타일을
만들고 템플릿 파일을 배포해봐도 사람마다 제각각의 폰트와 문단 정렬을 쓰기가
일쑤입니다. 나중에 부분부분 파일을 모아서 하나로 만들려면 폰트와 문단 정렬만
고치는 것도 큰 일이 되지요. 하지만 LaTeX을 쓰면 애초에 이렇게 하는 것이
어렵습니다.

전체적으로 줄여보면 LaTeX은 글쓰기의 기본에 집중할 수 있는 환경을 만들어 주는
장점이 크다고 할 수 있겠습니다. 여러분들이 여기 SteemIt에서 쓰시는 Markdown도
마찬가지 특성을 갖고 있다고 하겠습니다. 

### 수식 작성

말씀드렸듯이 LaTeX은 수식 작성이 아주 뛰어납니다. 수식 명령어로 수식을 조판해
내는데요. 아래아 한글이나 최근의 마이크로소프트 워드에서 지원하는 수식 명령이
바로 LaTeX에서 기원한 명령들입니다. 수식은 간단히 예를 몇가지 보겠습니다.

```latex
\begin{equation}
    a^2 + b^2 = c^2
\end{equation}
```

```latex
\begin{equation}
    \sum_{i=1}^{n} i = \frac{1}{2} n (n + 1)
\end{equation}
```

```latex
\begin{equation}
    x = \frac{-b \pm \sqrt{b^2 - 4ac}{2a}
\end{equation}
```

```latex
\begin{equation}
    \int f'(x)g(x) dx = f(x)g(x) - \int f(x)g'(x) dx
\end{equation}
```

LaTeX으로 컴파일 하면 다음과 같이 출력됩니다. 수식에 기본으로 (1), (2), (3)과
같이 수식 번호가 자동으로 붙음을 볼 수 있습니다. 이 역시 나중에 한번 쓴 수식을
다시 언급할 때 편리합니다. 물론, 수식 번호를 생략하는 명령어 옵션도
있겠습니다.

![Equations][/assets/2018-04-02-computing-for-scieng-students-04/equations-capture.png]


#### equation reference

### Table of Contents

### DocumentClass

### Reference (BibTeX)

## LaTeX 관련 정보

  * 책, 공짜 문서, ktug
  * 서비스: ShareLaTeX

## 마치며

문서도 컴퓨터 언어로 쓴다.
