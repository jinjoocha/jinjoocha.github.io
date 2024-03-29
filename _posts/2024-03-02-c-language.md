---
title: C 프로그래밍 - C 언어 기초
date: 2024-03-02 23:23:00 +0900
categories: [Blogging, C]
tags: [c]
pin: true
published: true
---

<!-- {: width="250" height="250" } -->
<!-- {: width="972" height="980" } -->
<!-- {: .prompt-tip } -->
<!-- {: .prompt-info } -->
<!-- {: .prompt-warning } -->
<!-- {: .prompt-danger } -->


## 프로그래밍 언어
인간과 컴퓨터의 대화에 사용되는 의사소통 수단.

## 컴파일러
컴퓨터가 이해할 수 있도록 기계어로 번역하는 역할을 수행.  
컴파일러가 번역한 어셈블리 코드를 **어셈블러**가 기계어로 변환하는 작업을 함.  

## C 언어
인간이 이해하기 쉬운 언어라 **고급언어(high-level language)** 라고 하나,  
하드웨어 제어가 가능하기 때문에  
컴퓨터가 이해하기 쉬운 언어인 **저급 언어(low-level language)**의 특성을 지닌 고급 언어라고 할 수 있음.


![스크린샷 2024-03-03 오전 1 33 23](https://github.com/jinjoocha/Programmers/assets/153695091/61a7db1f-cc31-42d0-b394-01e3bb06a03e){: width="700" height="600" }


### C 언어의 특징
- 저급 언어 특성을 가진 고급 언어
- 논리적이며 구조적인 시스템 프로그래밍 언어
- 하드웨어 제어가 가능
- 프로그램 이식성이 높음
- 간략한 문법 표현으로 함축적인 프로그램 작성이 용이함


## 프로그램 개발
프로그램 : 컴퓨터로 하여금 특정한 작업을 수행하도록 하는 명령어들의 집합.  

프로그램 작업을 수행하는 데는 반드시 요구되는 프로그램 2가지
- 에디터
- 컴파일러

### 에디터
: 소스코드를 쉽게 작성하여 기억장치에 저장할 수 있도록 도와주는 도구.

### 컴파일러
: 에디터를 사용하여 작성한 소스 코드를 컴퓨터가 이해할 수 있는 기계어로 바꾸는 번역 소프트웨어.

### 프로그램 개발 순서
1. 프로그램 목적 정의  
: 요구 분석과 시스템 분석을 통하여 프로그램이 가져야 할 기능 정의
2. 프로그램 설계  
: 분석된 기능을 처리할 수 있도록 프로그램 구조를 설계
3. 소스 코드 작성  
: 작성된 프로그램 설계를 기반으로 에디터를 사용하여 작성
4. 컴파일 / 링킹  
: 소스 코드를 실행 가능한 코드로 변환하고 문법 검사
5. 프로그램 실행  
: 프로그램 실행
6. 테스트와 디버깅  
: 에러를 검사하고 디버깅
7. 유지 보수  
: 사용 중 발생되는 에러나 추가적인 변경 사항을 처리

<br>

크게 **코딩 -> 컴파일 -> 링킹** 이라는 3단계의 변환 과정을 거쳐 완성됨.  
1. 코딩(coding) - 소스코드(source code)를 작성하여 소스파일(source file)을 생성하는 과정
2. 컴파일(compile) - 소스파일이 목적파일(object file)로 변환되는 과정
3. 링킹(linking) - 링커를 통해 목적파일을 실행파일(execution file)로 변환하는 과정  


## C 프로그램의 완성 과정

![IMG_E826B83E733E-1](https://github.com/jinjoocha/Programmers/assets/153695091/f12a983d-ee8d-4a01-8b8f-4bbbfd668316){: width="300" height="400" }

![IMG_CCFA59652752-1](https://github.com/jinjoocha/Programmers/assets/153695091/ba69960e-21cc-48f3-a242-c109d0a0d68e){: width="700" height="600" }


## C 프로그램의 기본 구조
- 반드시 하나 이상의 함수를 포함해야 함
- `main()` 함수가 반드시 존재해야 함
- 함수의 시작과 끝을 알리는 중괄호 `{}` 를 사용해야 함
- 중괄호 안에는 변수선언문, 치환문, 연산문, 함수 등의 명령을 기입함
- 선행처리기(preprocessor)를 제외하고, 문장의 끝에는 세미콜론 `;`을 붙임

## C 프로그램의 구성 요소
- 예약어 : int, char, if, for, ...
- 명칭 : 변수, 배열, 함수, ... 등의 이름
- 상수 : 값이 불변인 자료
- 연산자 : =, -, ++, *, /, ...
- 설명문(주석) : 프로그램에 대한 주석

### C언어 예약어 (reserved word)
- 자료형 관련
: char, int, float, short, long, double, unsigned, union, enum, void, ...
- 기억 관련
: auto, static, extern, register, ...
- 제어 관련
: if ~ else, for, while, do ~ while, switch ~ case, break, continue, return, ...
- 기타
: main, sizeof, include, ...

### 명칭 (identifier)
규칙을 지키자!
- 영문자와 숫자의 조합으로 만듦
- 첫 문자는 영문자나 밑줄 `_` 이어야 함
- 특수문자 사용금지 (밑줄은 가능~!)
- 문자 사이에 공백 금지
- 예약어 금지
- 영문자 대문자와 소문자는 서로 구별하여 사용
- 명칭의 길이는 컴파일러에 따라 차이가 있음 (일반적으로 32자까지 인식가능)


| 올바른 명칭           | 비 고              |
|:-------------------|:-----------------:|
| sun10              | 영문자와 숫자 조합 가능 |
| SUN10              | sun10과는 다른 명칭   |
| For                | 예약어 for과는 다름   |
| _sum               | 밑줄 사용 가능       |

| 잘못된 명칭           | 비 고               |
|:-------------------|:------------------:|
| 2m                 | 숫자로 시작 불가       |
| KBS@TV             | 특수문자 사용 불가      |
| for                | 예약어 사용 불가       |
| SUN 10             | 문자 사이 공백 사용 불가 |


![스크린샷 2024-03-10 오후 4 41 16](https://github.com/jinjoocha/basic_study/assets/153695091/a85af21a-3911-4379-be93-4449ac86cf50){: width="700" height="600" }

## 상수 (constant)
- 항상 고정된 값
- 값이 한 번 정해지면 프로그램 도중에 변경 불가
    - 정수형 상수  
    : 10진수, 8진수, 16진수로 표현 (+ unsigned형 상수, long형 상수)
    - 실수형 상수  
    : 부동소수점 상수, double형을 기본 자료형으로 사용
    - 문자형 상수  
    : 단일 인용부호('')로 묶여 있는 1개의 영문자나 숫자,  
    내부적으로는 해당문자의 ASCII 코드값이 사용,  
    Escape 문자 (키보드에 나타나 있지 않은 문자)
    - 문자열 상수  
    : 이중 인용부호("")로 묶여 있는 복수개의 영문자나 숫자,  
    기억공간에 보관될 때는 문자열 끝에 null 문자(\0)가 자동적으로 추가됨  
    <img width="1230" alt="스크린샷 2024-03-10 오후 5 01 53" src="https://github.com/jinjoocha/basic_study/assets/153695091/a89ba823-22fb-45b3-965c-537420be3acc">{: width="400" height="300" }_총 12개의 기억 공간이 소요가 된다!_


## 변수 (variable)
- 변할 수 있는 값
- 프로그램에서 변수는 프로그램 실행 도중 변할 수 있는 값이 저장되는 기억공간을 의미
- 예를 들어 `i = 10;`에서 `i`는 변수(명)이고, `10`이란 값을 `i`라는 이름으로 정의된 기억공간에 저장한다는 의미
- 이러한 변수 속에 들어가는 값은 수시로 변경될 수 있음
- 변수는 사용 전에 반드시 선언하여, 컴파일러가 기억공간에서 일정공간을 확보할 수 있도록 해야 함


### 변수의 특징
- 모든 변수는 이름이 있음 (변수명)
- 모든 변수는 정해진 자료형이 있음
- 모든 변수는 할당된 값을 갖음


### 변수명의 정의 규칙
- 모든 변수는 사용되기 전에 선언되어야 함
- 반드시 영문자나 밑줄로 시작해야 함
- 중간에 숫자, 밑줄을 섞어서 명명할 수 있음
- 중간에 밑줄 이외에 특수문자를 섞어서 명명할 수 없음
- 대, 소문자를 구별하여 사용함
- 예약어 사용 금지

### 변수의 초기화
: 최초의 어떤 값이 부여된 것을 초기화 했다고 얘기 함

```c
#include <stdio.h>

void main() {
    int i, sum;
    for (i=1; i<=10; i++) // 변수 i를 초기화 함
        sum=sum+i; // 변수 sum은 위에 선언만 했고, 초기화 안하고 바로 갖다씀
    printf("1부터 10까지의 합=%d\n", sum);
}
```


`1부터 10까지의 합=55 // 출력결과`



## 자료형의 종류
<img width="1249" alt="스크린샷 2024-03-10 오후 5 13 25" src="https://github.com/jinjoocha/basic_study/assets/153695091/11aecbdd-79c2-4f7f-89c6-a0d9d040125b">{: width="700" height="600" }


## 선행처리기 (preprocessor)
: 컴파일에 앞서 프로그램 선두에 선언된 지시자들을 미리 처리하는 역할을 수행

### 선행처리기의 종류

| 선행처리기                  | 기능          |
|:-------------------------|:------------:|
| #include                 | 파일 포함      |
| #define                  | 매크로 정의     |
| #if #else #elif #endif   | 조건부 컴파일   |

### 주의사항
- 반드시 `#` 으로 시작해야 함
- 명령문 끝에는 세미콜론 `;` 을 붙이지 않음
- 한 줄에 하나의 명령만 씀
- 소스 프로그램의 첫 부분에 위치



ㄱㄱ~!


## 테스트

```c
#include <stdio.h>

int main(int argc, const char * argv[]) {
    // insert code here...
    printf("Hello, World!\n");
    return 0;
}
```

```c
int a, b, c;
int product(int x, int y);

int main(void) {
    printf("Enter a number between 1 and 100 : ");
    scanf("%d", &a);
    
    printf("Enter another number between 1 and 100 : ");
    scanf("%d", &b);
    
    c = product(a, b);
    printf("%d * %d = %d \n", a, b, c);
}

int product(int x, int y) {
    return (x * y);
}
```


## 참고
(도서) C 프로그래밍 - 김형근, 곽덕훈, 정재화