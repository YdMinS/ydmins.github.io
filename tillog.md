---
layout: page
title:  "TIL LOG"
date:   2023-01-02
excerpt: "Today I Learned Log."
project: true
tag:
- TIL
- JAVA
comments: true
---


# TIL LOG란?
TIL이란 "Today I Learned"의 약자로 오늘 배운 것들을 기록하는 개발자들의 기록의 한 형태이다. 여기다 LOG를 붙인 이유는 이 페이지를 인덱스와 같은 페이지로 활용하기 위함이다. 다시말해서 어떤 공부를 했는지 간단하게는 기록하지만 자세한 내용들은 내용의 종류에 따라서 다양한 매체에 기록할 예정이다.

## TIL LOG 사용방법
TIL LOG는 그날 배운 내용들을 세세히 기록하기 보단 큰 흐름의 기록이다. 따라서 각 내용의 자세한 내용은 https://ydmins.com 에 방문해서 날짜 또는 주제를 검색해서 찾아볼 수 있다.

<details>
<summary>2023년 1월</summary>
<div markdown="1">       
#### 2023-01-02 MON
1. 패스트캠퍼스 - 스프링의 정석 강의를 들었다.
  - MySQL 작동안하는 이슈가 있었다.
  - Bean 관련 또는 3과 전체 복습이 필요해 보인다.

2. GITHUB을 이용해서 TIL용 블로그를 만들었다.
  - 개발 공부 일기쓰듯이 사용할 계획이다.
    
#### 2023-01-03 TUE
1. 스프링의 정석 Chpater3 처음부터 다시 듣기 시작했다.
  - Spring DI에 대해 배우기 시작했다.
  - 변경에 유리한 코드를 작성하기 위해 분리를 잘 해야 한다. 분리하는 방법에는 3가지가 있다. 
    1. 변하는 것과 변하지 않는 것을 구분
    2. 관심사에 따라서 구분
    3. 중복코드를 분리
  - Properties 객체는 파일을 불러오고 저장하는 등에 편리함이 있어서 사용한다.
2. ydmins.github.io 수정했다.
  - 어제 처음으로 github.io 블로그를 만들 때는 많이 낯설었는데 오늘은 확실히 좀 더 보였다. 확실히 할수록 나아진다.

#### 2023-01-04 WED
1. 스프링의 정석 Chapter3 Spring DI 개념을 이해하기 위한 기초강의를 다 들었다.
    - 객체 컨테이너 (ApplicationContext)에 대해 배웠다.
        - 객체들을 Map에 넣어두고 사용하는 기능이다.
        - 객체를 자동으로 등록하는 @Component
        - 객체를 이름을 이용해 자동으로 찾아서 연결해주는 @Resource
        - 객체를 타입을 이용해서 자동으로 찾아서 연결해주는 @Autowired 를 알게되었다.
        - Annotaion 사용시 장점
            - 작성해야 할 코드 줄어든다. -> 관리해야 할 코드 줄어든다. & 실수가 줄어든다
    

  - 아직 Spring DI를 잘 이해 못한것 같다.

#### 2023-01-05 THU
1. 스프링의 정석 Chpater3 Spring DI 개념을 제대로 들어가기전 일단 한 번 써보기를 했다.
    - xml 파일을 이용해서 Beans 태그 내에 Bean들을 정의해 보았다.
        - Bean 태그 사이에 내용들
            - property
                Setter가 정의되어 있을 경우에 사용 가능하다.
            - contructor-arg
                생성자가 선언되어 있을 경우에 사용 가능하다.
    - 강의를 듣는 내내 bean을 왜 굳이 만드는 것일까?란 물음이 계속 들었다.
        - 다음 강의 초반 부분만 살짝 들었는데, Bean이라는 것이 재사용 가능한 Component, 상태(Intance Variable), Getter, Setter, No-Args-Constroctor를 따로 저장해 둔 것이라고 한다. 즉, 오늘까지 이해한 바로는 계속 사용해야 할 것들을 콩속에 넣어두고 필요할 때마다 꺼내쓰도록 만든것이 bean이라는 것이다.
    

#### 2023-01-06 Fri
1. 스프링 정석 Chapter3 Spring DI 개념을 제대로 시작했다.
    - Bean은 Spring Container가 관리하는 객체이다.
    - Spring Container는 Bean의 저장소이자 관리자(생성, 소멸, 연결)이다.
2. Application Context에 대해서 배웠다.
    - TIL을 기록하다 보니 Spring Container에서 왜 갑자기 Application Context로 넘어왔는지 모른다는 점을 발견했다.
    - 줄여서 AC라고한다.
    
#### 2023-01-07 Sat
1. 스프링 정석 Chapter3 Spring DI 강의를 다 들었다.
    - 지난번에 파악을 못한 ApplicationContext를 이해하게 됐다.
        - XMl을 이용해서 ApplicationContext에 저장할 Bean들을 설정한다.
        - @Component Annotation을 사용하면 XML을 작성하지 않고 ApplicationContext에 Bean을 설정할 수 있다.
        - @Autowired 또는 @Resource를 사용하면 ApplicationContext에 저장되어있는 객체를 주입해서 사용할 수 있다.
            - @Autowired는 타입으로 객체를 검색한다. 만약 같은 타입의 객체가 여러개 있다면 이름이 같은 것을 찾는다.
            - @Resource는 이름으로 객체를 검색한다. 일치하는 이름의 객체가 없다면 예외가 발생한다.
    - Spring DI란
        - ApplicationContext에 저장되어 있는 Bean을 호출할 때 Bean이 사용할 객체를 전달해 주는 것을 "의존성 주입 (Dependency Injction)"이라 한다.
        - 즉, DI의 의존성은 Bean의 관점이다.

#### 2023-01-09 Mon
1. 스프링 정석 Chpater2 관심사의 분리와 MVC 패턴에 대한 강의를 들었다.
    - 코드를 입력, 처리, 출력으로 분리 시켜 작성하는 코드는 처리에 집중할 수 있다.
    - 이 때 처리부분의 코드를 Controller라고 한다. 
    - Controller에서 처리한 결과를 Model 객체에 담아둔다.
    - 이 Model의 데이터를 기반으로 View 영역이 결과물을 출력해준다.
    - MVC란?
        - 관심사의 분리를 통해 코드를 Controller(처리영역)과 View(출력영역)으로 나누고 그 두 영역에 데이터를 전달하기 위해 Model이라는 데이터 전달 객체를 도입한 코딩 방식이다.
    
#### 2023-01-10 Tue
1. 스프링 정석 Chpater2 서블릿과 JSP에 대해한 강의를 들었다.
    - Servlet은 Spring의 Controller와 RequestMapping을 함께 쓰는 것과 같다.
    - JSP는 요청시 Servlet으로 변환된다.
    - Servlet에 대해서 여러가지를 배웠지만 Servlet자체가 무엇인지에 대한 답은 찾지 못했다.
    - 내장객체 (Implicit Obejcts)에 대해서 배웠다.
</div>
</details>
