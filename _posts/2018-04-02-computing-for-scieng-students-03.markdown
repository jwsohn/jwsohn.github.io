---
layout: post
title:  "이공계 대학생/대학원생을 위한 컴퓨팅 강좌 3: 리눅스(Linux)에서 내가 만든 프로그램을"
date:   2018-03-28 22:30:00 -0500
published: yes
categories: 강좌
---

# 이공계 대학생/대학원생을 위한 컴퓨팅 강좌 3: 리눅스(Linux)에서 내가 만든 프로그램을

안녕하세요. @jwsohn입니다. 오늘 강좌에서는 리눅스에서 프로그램을 개발하는
방법과 LaTeX으로 이공계 관련 문서 작성을 간단히 해 보겠습니다. 오늘 강좌를
통해서 리눅스 상에서 프로그램 개발이 왜 편리한지, 그리고 LaTeX으로 문서를
작성하는 것이 왜 효율적인지 전달(?)이 될 수 있으면 좋겠습니다.

## 프로그램 만들기

어떤 컴퓨터 언어를 배우더라도 제일 처음에는 소위 "Hello, World!" 프로그램을
작성합니다. 단순히 "Hello, World!" 메세지를 화면에 출력하는 프로그램인데요.
이를 통해 해당 컴퓨터 언어의 특성을 간단히 한 눈에 볼 수 있기 때문입니다.

일단 리눅스에서 바로 사용 가능한 다양한 언어로 "Hello, World!" 프로그램을
만들어 보겠습니다.

### Python: hello.py
```python
#!/usr/bin/env python

print "Hello, World!"
```

### C: hello.c
```c
#include <stdio.h>

void main()
{
    printf("Hello, World!\n");
}
```

### Java: HelloWorld.java
```java
public class HelloWorld
{
    public static void main(String[] args)
    {
        System.out.println("Hello, World!");
    }
}
```

### Perl: hello.pl
```perl
#!/usr/bin/env perl

print "Hello, World!";

```

### LaTeX: hello.tex
```latex
\documentclass[a4paper]{article}

\begin{document}
Hello, World!
\end{document}
```

## 리눅스에서 프로그램 실행 방법 

일단 여러분들이 학교 전산소 같은 곳에서 리눅스 계정을 하나 구했다고
가정하겠습니다. 

### 에디터 (editor) 사용: nano

hello.py 에디팅 설명

### 실행 방법

### Python
```
python hello.py
```

### C
```
gcc hello.c -o hello
./hello
```

### Java
```
javac HelloWorld.java
java HelloWorld
```

### Perl
```
perl hello.pl
```

### LaTeX
```
pdflatex hello.tex
```

## LaTeX 문서 만들기

### 수식 만들기

### 리포트 만들기 

#### Comparison with Markdown

#### Table of Contents 


