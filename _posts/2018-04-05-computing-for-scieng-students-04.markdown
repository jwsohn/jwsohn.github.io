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
마크다운(Markdown)과 비슷한 문법을 쓰기 때문에 스티미언들은 더 친숙하게 배울 수
있는 장점이 있습니다.


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

지금까지 예를 보면 LaTeX이나 Markdown 모두 **문서에 명령어를 추가(markup)**해서 글자
모양이나 문서 포맷을 지정하는 것을 알 수 있습니다. 그러면, 저번 포스팅에서
간단히 언급했던 Hello, World! 문서 만들기로 다시 돌아가 보겠습니다.

### Hello, World!

```latex
\documentclass[a4paper]{article}

\begin{document}
Hello, World
\end{document}
```

### Headings

여기에 위에서 배운 글제목을 넣어 보겠습니다.

### 문서 기본 템플릿 (template)

article 이외에 report, book 등이 있습니다.

### 수식 작성

```latex
a^2 + b^2 = c^2
```

#### inline

#### equation reference


### Table of Contents

### DocumentClass

### Reference (BibTeX)

## LaTeX 관련 정보

  * 책, 공짜 문서, ktug
  * 서비스: ShareLaTeX

## 마치며

문서도 컴퓨터 언어로 쓴다.
