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

일단 이 정도까지는 다들 잘 하십니다. 들여쓰기와 코드 블록(code block)
맞추기지요.

```java
public class HelloWorld
{
    public static void main(String[] args)
    {
        System.out.println("Hello, World!");
    }
}

```

```python
#!/usr/bin/env python

print "Hello, world!"

```

그런데 이 다음부터 제각각이 됩니다. 변수 (variable)에 이름을 줘 볼까요? Java는
lowerCamelCase 형식을 따르고 Python은 snake_case를 따릅니다. 

Java:
```java
public class HelloWorld
{
    public static void main(String[] args)
    {
        String helloWorldMessage = "Hello, World!";
        System.out.println(helloWorldMessage);
    }
}
```

Python:
```python
#!/usr/bin/env python

hello_world_message = "Hello, world!"
print hello_world_message

```

물론, 위의 경우 Java에서 `hello_world_message` 이름의 변수를 써도 되고
Python에서 `helloWorldMessage` 이름의 변수를 써도 프로그램 수행에는 아무런
지장이 없습니다. 물론 `Helloworldmessage`니 `HELLO` 같은 이름을 마음대로 줘도
됩니다.

하지만, 여기서 Java의 경우는 lowerCamelCase로 변수명을 쓰기로 *개발자들간에*
관습을 만들었고 Python의 경우는 snake_case로 단어 사이에 `_`를 넣어서 변수명을
쓰기로 했다는 점을 중요하게 보셔야 하겠습니다.

참고로 Java코드에서 프로그램 전체의 이름인 class 이름은 `HelloWorld`로
UpperCamelCase 방식을 썼음을 알 수 있습니다. 이런 세세한 것까지 신경을 써야
하는 것이죠.

그리고 변수(variable)에 값(value)를 저장하는 = 연산자 주위에 공백을 하나씩
넣은 것도 주의깊게 보셔야 합니다. 그러니까 `helloWorldMessage="Hello,
World!";`와 같은 표현을 쓰는 것은 지양한다는 것이죠. 

왜 이런 것까지 세세하게 따질까요? 연산이 조금만 복잡해지만 이렇습니다. 0 부터 9까지
화면에 출력하는 프로그램을 만들어 보죠. 변수 `i`를 0부터 시작해서 10보다 작은
경우 계속 1 씩 증가시키며 `System.out.println(i);`를 실행하는 코드입니다.

Java:
```java
public class PrintNumbers
{
    public static void main(String[] args)
    {
        for (int i = 0; i < 10; ++i)
        {
            System.out.println(i); 
        }
    }
}
```

여기서 `for (int i = 0; i < 10; ++i)` 부분을 보겠습니다. 컴파일러 입장에서는
아래 세 문장이 똑같습니다. 하지만 사람 눈에는 `=`나 `<` 연산자 주위에 공백을
적절히 쓴 제일 윗 문장이 가장 가독성이 좋기 마련입니다.
 
  * `for (int i = 0; i < 10; ++i)`
  * `for (int i=0;i<10;++i)`
  * `for (int i = 0 ; i < 10 ; ++ i)`

이것 말고도 코딩 스타일에 대해서는 쓸 말이 무지하게 많습니다만 일단 간단히
여기서 줄이구요. 다시 한번 코딩 스타일 습관은 **다른 사람도 읽기 좋은** 코드를
만드는데 필수불가결이라는 사실을 꼭 기억하시기 바랍니다. 또한, **다른 사람이
짠 코드와 내 코드를 섞을 때** 같은 코딩 스타일을 쓰는 것이 얼마나 생산성을
향상시키는 가도 나중에 꼭 경험해 보시기 바랍니다.

참고로 많이 쓰이는 Java와 Python의 코딩 스타일 가이드를 링크해 봅니다.

  * [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)
  * [Python pep8 style guide](http://pep8.org)


### 에디터(Editor): 처음에는 Linux에서 `vim`이나 `emacs`를 쓰자

일반적으로는 코딩을 배울 때 처음부터 자바(Java)의 이클립스(Eclipse)와 같이
에디터(editor), 컴파일러(compiler), 디버거(debugger)가 통합된 통합환경(IDE,
integrated development environment)을 쓰는 경우가 많은 것 같습니다. 일견
통합환경은 직관적인 사용자 인터페이스와 컴파일, 디버깅 작업을 자동으로 처리해
주는 까닭에 코딩 초보자에게 좋을 것 같지만 제가 보기에는 프로그램 개발 과정을
편리함으로 추상화 시키는 까닭에 초보자에게는 그다지 좋지 않다고 생각합니다. 
또한, 초보자가 쓰기에는 지나치게 기능이 많기도 합니다.

그럼 어떤 개발환경을 쓰는 것이 좋을까요? 처음 코딩을 하시는 분들은 리눅스
서버에 리눅스 명령 프롬프트 (CLI, command line interface)로 접속해서 텍스트
에디터(text editor)를 이용해 프로그래밍을 시작하시는 것을 추천합니다. 명렁어를
하나하나 손으로 타이핑하면서 어플리케이션 개발의 전체적 과정을 익히는 것이
필요하기 때문입니다. 특히, 처음에는 컴파일 작업을 손으로 해서 어떤 파일을
컴파일 시키면 어떤 형태의 실행 파일이 나오는지 알아야 하겠습니다.

그리고 겉보기와는 달리 터미널과 같은 텍스트에서 쓰는 에디터들이 조금만
사용법을 배우면 쓰기가 편해지는 특성이 있습니다. 대표적인 것이 `vim`과 `emacs`
에디터의 양대산맥인데요. 어떤 에디터를 쓰시든지 상관은 없습니다만 두 에디터
모두 기본적으로 마우스를 쓰지 못하고 키보드 명령어를 하나하나 익히셔야 하는
불편이 있습니다. 

`vim`의 경우는 또 문화적인 충격(?)도 있습니다. 에디터를 실행시키고 나서 키를
눌러보면 타이핑이 안됩니다. 이것은 `vim` 에디터가 기본적으로 편집 모드와
명령어 모드를 구분하기 때문인데요. `i` 키를 눌러 명령어 모드에서 편집 모드로
진압해야 타이핑이 가능하겠습니다.

명령어 모드에 대해 간단히 설명을 드리면 이렇습니다. `vim`에서는 커서 이동키가
`h`, `j`, `k`, `l` 입니다. 그러니까 같은 `j`라도 명령어 모드에서는 아랫쪽
커서키가 되고 편집 모드에서는 j 글자가 되는 것이죠. 

![hjkl keys in vi](/assets/2018-04-14-computing-for-scieng-students-06/hjkl.jpg)

이런 `vim`에서 명령어 모드와 편집 모드의 구분은 조금만 습관이 되시면 아주
편리해지는 기현상(?)을 경험하실 수 있습니다. 일례로 `j`, `k` 키로 커서를
아래위로 이동하는 것이 키보드 오른쪽에 치우친 커서키로 손을 뻗는 것보다
편리하기 마련이지요. 

제가 `vim` 사용자이다보니 `vim` 얘기가 길어지고 있는데요. `emacs` 역시 좋은
에디터입니다. `emacs`는 에디터이지만 그 기능이 방대하기 때문에 어떻게보면
통합환경보다 더 나은 개발 환경을 제공한다고 볼 수도 있겠습니다. `emacs`는
제가 기초 이상을 잘 모르는 까닭에 일단 소개만으로 그치겠습니다.

참고로 리눅스 명령어 프롬프트에서 커서 이동 명령은 `emacs` 단축기를
이용합니다. ctrl-a가 Home 키 역할을, ctrl-e가 End 키 역할을 합니다.
ctrl-p는 위쪽 화살표 키 역할, ctrl-n은 아랫쪽 화살표 키 역할입니다.

그리고 Python을 쓰시는 분들은 에디터에 추가해서 Python 명령어 한 줄 단위로
바로바로 실행시켜볼 수 있는 인터프리터(interpreter) 역시 중요하겠지요. 기본으로
제공되는 `python` 인터프리터보다는 `ipython` 인터프리터를 쓰시길 추천합니다.
기본적으로 명령어에 색깔을 입혀주는 syntax highlighting, 탭 키를 누르면 가장
가까운 명령어나 변수 이름을 알아서 추측해주는 name completion 기능이
제공됩니다.

마지막으로 처음에 `vim`이나 `emacs`에 아무래도 적응이 안되시는 분들은 제가
전에 잠깐 언급한 `nano` 에디터를 쓰시길 추천합니다. 그리고, Eclipse와 같은
통합환경은 개발하는 프로젝트의 크기가 커지면서 소스 코드 파일의 숫자가
많아지면 그때부터 쓰시면 되겠습니다. 변수나 클래스, 모듈 이름을 하나만 고치면
소스코드 전체에 걸쳐서 자동으로 고쳐주는 refactoring 같은 기능은 통합환경을
써야 편리하게 이용할 수 있으니까요.

## 다른 개발자와의 협업(collaboration)
 
### 개발 문서 작성하기: 주석(comment)을 달자

주석(comment)의 바른 예: [출처](https://www.tutorialspoint.com/java/java_documentation.htm)

```java
/**
 * The HelloWorld program implements an application that
 * simply displays "Hello, World!" to the standard output.
 *
 * @author  foobar
 * @version 1.0
 * @since   2018-04-16 
 */

public class HelloWorld
{
    public static void main(String[] args)
    {
        /* Prints Hello, World! on standard output. */

        String helloWorldMessage = "Hello, World!";     // assigns "Hello, World!" 
        System.out.println(helloWorldMessage);
    }
}
```

우선, 소스 코드 내부에 주석(comment)을 많이 다는 습관을 들이셔야 합니다.
최고의 comment는 잘 만든 소스 코드라는 얘기가 있기는 하지만 그 정도의 고품질
소스 코드를 만들어 내는 사람들은 지극히 드뭅니다. 따라서, 기본적으로 설명이
필요할 때마다 comment를 다는 습관을 들이는 것이 좋습니다.

코딩을 하다 보면 누구나 경험하게 되는 것이 이렇습니다. 일이년 정도 지나서
자신이 짠 소스 코드를 보면 감이 오질 않습니다. 이럴 때 comment도 없으면
난감하죠. 정말로 내가 짠 코드를 내가 못 알아보는 황당한 상황이 전개되니까요.
하지만, 사람은 망각의 동물입니다. 내가 쓴 코드를 잘 활용하려면 comment를 잘
다는 것이 일상이 되어야 합니다. 하물며 남이 보게 될 코드라면 더더욱 comment에
신경을 써야 하겠지요.

### GitHub.com을 사용하자

![Github.com](/assets/2018-04-14-computing-for-scieng-students-06/github.jpg)

그 다음으로 오픈 소스 프로젝트 호스팅 서비스인 GitHub.com에 내 프로젝트
페이지를 개설한 다음 개발 문서를 써 보기를 추천합니다. 처음에는 개발 문서라고
해도 프로젝트 소개인 Readme.md(md는 markdown의 줄임입니다)를 쓰는 것이
대부분이겠습니다만 **다른 사람이 읽어볼 필요**가 있는 개발 문서를 작성해
본다는 것에 큰 의미가 있습니다. 게다가, GitHub의 문서 포맷은 기본적으로
스팀잇과 동일한 markdown을 사용합니다. 

GitHub.com에 프로젝트 페이지를 오픈하기 위해서는 소스 코드 버전 관리를
담당하는 `git` 명령어 사용방법을 배워야 합니다. `git` 명령으로 소스코드를
업로드/다운로드 하는 것이 생소하고 복잡할 수 있습니다만 다른 개발자와의 협업을
하려면 언젠가는 반드시 습득해야 하는 것이 `git` 명령입니다. 우선, 혼자만 쓰는
프로젝트라도 `git` 명령으로 프로젝트 저장소 (repository)에 소스 코드 변경
사항을 체크인(checkin)/체크아웃(checkout)을 하는 습관을 들여볼 필요가
있습니다.

GitHub 사용 방법 강좌로는 아래 링크를 추천합니다. 

  * [GitHub For Beginners: Don’t Get Scared, Get Started](https://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1/)

## 마치며

지금까지 코딩을 배우는데 도움이 되는 습관과 여기에 필요한 도구들에 대해 간단히
알아봤습니다. 전체적으로 코딩 스타일과 같이 코딩에 직접적으로 연관이 되는
습관과 개발 도큐먼트 작성과 같이 코딩을 도와주는 습관으로 나눌 수 있겠습니다.

적절한 코딩 스타일을 갖춘 코드를 작성하는데는 개발 도구의 도움이 필요한데요.
처음 시작하실 때는 Eclipse와 같은 통합환경(integrated development
environment)보다 터미널 모드에서 vim이나 emacs 에디터를 써서 코딩을 하기를
추천드립니다. 

개발 문서 작성과 소스코드 버전 관리를 위해서는 github.com에 프로젝트를
개설하고 `git` 명령을 이용해서 소스코드 관리를 하는 습관을 들이는 것을
추천합니다. 장기적으로 github.com에 올라와 있는 다른 개발자들과
협업(collaboration)을 하는 방법을 처음부터 습득할 수 있겠습니다.

읽어 주셔서 감사합니다. 다음 글에서 또 뵙겠습니다.

