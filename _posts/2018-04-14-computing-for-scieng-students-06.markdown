---
layout: post
title:  "이공계 대학생/대학원생을 위한 컴퓨팅 강좌 6: "
date:   2018-04-14 22:30:00 -0500
published: no
categories: 강좌
---

# 이공계 대학생/대학원생을 위한 컴퓨팅 강좌 6: 코딩에 도움이 되는 습관

안녕하세요 @jwsohn입니다. 이번 포스팅에서는 코딩에 도움이 되는 습관과 좋은
습관을 들이는데 도움이 되는 추가 도구(tool)들에 대해 알아보도록 하겠습니다.

## 코딩에 도움이 되는 습관

코딩은 글쓰기와 비슷한 속성을 갖고 있습니다. 우선, 코딩은 글쓰기처럼 명령어를
하나 하나 작성해야(write) 합니다. 단어들이 이루어져 문장을 이루고, 문장이 모여
문단, 글이 되듯이 코딩 역시 statement들이 모여서 block을 만들고 이것이 불러
쓰기에 용이한 function이나 class를 이루게 되지요. 이것들이 더 모이면
module이나 완성된 application이 될 것이구요.

글쓰기에서 글의 전체적인 구조가 중요하듯이, 코딩 역시 마찬가지입니다. 그런데
이런 구조적인 코딩 실력은 단기간에 길러지지 않습니다. 따라서 코딩을 잘 하려면
장기적인 노력이 필요하고 장기적인 노력을 들이기 위해서는 처음부터 좋은 습관을
기르는 것 역시 중요하겠습니다.

## 코딩 스타일(Coding style)

### Coding style guide

코딩 스타일은 처음부터 습관을 잘 들이셔야 합니다. 코딩 스타일이 좋지 않은
코드를 만들어 내면 그것으로서 그 코드의 수명(life cycle)은 끝이라고 보시면
되겠습니다. 다른 사람들이 편하게 읽을 수 있는 코드를 짜는 것은 처음부터 습관을
제대로 들이지 않으면 안되겠습니다. 코딩 스타일이 나쁜 경우 심지어는 내가 쓴
코드를 나중에 다시 봐도 감이 안오는 사태(?)가 벌어지기도 합니다.

그런데 코딩 스타일은 어느 정도까지 신경을 써야 할까요? 기본적으로 **글자
한자한자, 공백 하나하나까지** 신경을 쓰셔야 합니다. 간단히 예를 한번
보겠습니다.

### 구체적으로

  * indentation
  * spacing
  * namingConvention
    - include fileNames as well
  * comments
  * and blank lining

### 에디터(Editor): Linux에서 `vim`이나 `emacs`를 쓰자

일반적으로는 코딩을 배울 때 처음부터 자바(Java)의 이클립스(Eclipse)와 같이
에디터(editor), 컴파일러(compiler), 디버거(debugger)가 통합된 통합환경(IDE,
integrated development environment)을 쓰는 경우가 많습니다. 통합환경은
직관적인 사용자 인터페이스와 컴파일, 디버깅 작업을 자동으로 처리해 주는 까닭에
코딩 초보자에게도 좋을 것 같지만 오히려 프로그램 개발 과정을 추상화 시키는
까닭에 초보자에게는 좋지 않다고 생각합니다. 

그럼 어떤 개발환경을 쓰는 것이 좋을까요? 처음 코딩을 하시는 분들은 리눅스
서버에 리눅스 명령 프롬프트 (CLI, command line interface)로 접속해서 텍스트
에디터(text editor)를 이용해 프로그래밍을 시작하시는 것을 추천합니다. 명렁어를
하나하나 손으로 타이핑하면서 어플리케이션 개발의 전체적 과정을 익히는 것이
필요하기 때문입니다. 특히, 처음에는 컴파일 작업을 손으로 해 봐야 하겠습니다.

그리고 터미널과 같은 텍스트에서 쓰는 에디터들이 코딩에 강력한 성능을
발휘합니다. 대표적인 것이 `vim`과 `emacs` 에디터의 양대산맥인데요. 어떤
에디터를 쓰시든지 상관은 없습니다만 두 에디터 모두 기본적으로 텍스트 모드에서
작동하는 까닭에 명령어를 하나하나 익히셔야 하는 불편이 있습니다.

`vim`의 경우는 또 문화적인 충격(?)도 있습니다. 에디터를 실행시키고 나서 
키를 눌러보면 타이핑이 안됩니다. 이것은 `vim` 에디터가 기본적으로 편집
모드와 명령어 모드를 구분하기 때문인데요. `i` 키를 눌러야 명령어 모드에서
편집 모드로 진압하면서 타이핑이 가능하겠습니다.

명령어 모드에 대해 간단히 설명을 드리면 이렇습니다. `vim`에서는 커서 이동키가
`h`, `j`, `k`, `l` 입니다. 그러니까 같은 `j`라도 명령어 모드에서는 아랫쪽
커서키가 되고 편집 모드에서는 j 글자가 되는 것이죠. 

이런 `vim`에서 명령어 모드와 편집 모드의 구분은 조금만 습관이 되시면 아주
편리해지는 기현상(?)을 경험하실 수 있습니다. 일례로 `j`, `k` 키로 커서를
아래위로 이동하는 것이 키보드 오른쪽에 치우친 커서키로 손을 뻗는 것보다
편리하기 마련이지요. 

제가 `vim` 사용자이다보니 `vim` 얘기가 길어지고 있는데요. `emacs` 역시 좋은
에디터입니다. `emacs`는 에디터이지만 그 기능이 방대하기 때문에 어떻게보면
통합환경보다 더 나은 개발 환경을 제공한다고 볼 수도 있겠습니다. `emacs`는
제가 기초 이상을 잘 모르는 까닭에 일단 소개만으로 그치겠습니다.

참고로 리눅스 명령어 프롬프트에서 커서 이동 명령은 `emacs` 단축기를
이용합니다. `ctrl-a`가 Home 키 역할을, `ctrl-e`가 End 키 역할을 합니다.
`ctrl-p`는 위쪽 화살표 키 역할, `ctrl-n`은 아랫쪽 화살표 키 역할입니다.

그리고 Python을 쓰시는 분들은 Python 명령어 한 줄 단위로 바로 실행시켜볼 수
있는 인터프리터(interpreter) 역시 중요하겠지요. 기본으로 제공되는 `python`
명령보다는 `ipython` 인터프리터를 쓰시길 추천합니다. 기본적으로 명령어에
색깔을 입혀주는 syntax highlighting, 탭 키를 누르면 가장 가까운 명령어나 변수
이름을 알아서 추측해주는 name completion 기능이 제공됩니다.

마지막으로 처음에 `vim`이나 `emacs`에 아무래도 적응이 안되시는 분들은 제가
전에 잠깐 언급한 `nano` 에디터를 쓰시길 추천합니다. 그리고, Eclipse와 같은
통합환경은 개발하는 프로젝트의 크기가 커지면서 소스 코드 파일의 숫자가
많아지면 그때부터 쓰시면 되겠습니다. 변수나 클래스, 모듈 이름을 소스코드에
걸쳐서 자동으로 고쳐주는 refactoring 같은 기능은 통합환경을 써야 편리하게
이용할 수 있으니까요.

## 다른 개발자와 같이 일하기 (Collaboration)

### 개발 문서 작성하기 (documentation writing)
  * GitHub
    - start from writing Readme.md
  * markdown especially good for coding documentations
    - github.io

### Code sharing: open source project
  * Open source project: 남의 코드 고쳐 써 보기
  * Github again
  * Use git: 과거에는 patch

## Statistics
  * 5xx level graduate courses
  * important concepts: distributions, independence, dependence, joint
    probability, conditional probability
  * Data mining
  * Basic Stat theory
  * Mathematics
    * Linear algebra

