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

#### 2023-01-02
1. 패스트캠퍼스 - 스프링의 정석 강의를 들었다.
  - MySQL 작동안하는 이슈가 있었다.
  - Bean 관련 또는 3과 전체 복습이 필요해 보인다.

2. GITHUB을 이용해서 TIL용 블로그를 만들었다.
  - 개발 공부 일기쓰듯이 사용할 계획이다.

<details>
<summary>2023년 1월</summary>
<div markdown="1">       
    
    #### 2023-01-03
1. 스프링의 정석 Chpater3 처음부터 다시 듣기 시작했다.
  - Spring DI에 대해 배우기 시작했다.
  - 변경에 유리한 코드를 작성하기 위해 분리를 잘 해야 한다. 분리하는 방법에는 3가지가 있다. 
    1. 변하는 것과 변하지 않는 것을 구분
    2. 관심사에 따라서 구분
    3. 중복코드를 분리
  - Properties 객체는 파일을 불러오고 저장하는 등에 편리함이 있어서 사용한다.
2. ydmins.github.io 수정했다.
  - 어제 처음으로 github.io 블로그를 만들 때는 많이 낯설었는데 오늘은 확실히 좀 더 보였다. 확실히 할수록 나아진다.

#### 2023-01-04
1. 스프링의 정석 Chapter3 Spring DI 개념을 이해하기 위한 기초강의를 다 들었다.
    - 객체 컨테이너 (ApplicationContext)에 대해 배웠다.
        - 객체들을 Map에 넣어두고 사용하는 기능이다.
        - 객체를 자동으로 등록하는 @Component
        - 객체를 이름을 이용해 자동으로 찾아서 연결해주는 @Resource
        - 객체를 타입을 이용해서 자동으로 찾아서 연결해주는 @Autowired 를 알게되었다.
        - Annotaion 사용시 장점
            - 작성해야 할 코드 줄어든다. -> 관리해야 할 코드 줄어든다. & 실수가 줄어든다
    

  - 아직 Spring DI를 잘 이해 못한것 같다.

#### 2023-01-05
1. 스프링의 정석 Chpater3 Spring DI 개념을 제대로 들어가기전 일단 한 번 써보기를 했다.
    - xml 파일을 이용해서 Beans 태그 내에 Bean들을 정의해 보았다.
        - Bean 태그 사이에 내용들
            - property
                Setter가 정의되어 있을 경우에 사용 가능하다.
            - contructor-arg
                생성자가 선언되어 있을 경우에 사용 가능하다.
    - 강의를 듣는 내내 bean을 왜 굳이 만드는 것일까?란 물음이 계속 들었다.
        - 다음 강의 초반 부분만 살짝 들었는데, Bean이라는 것이 재사용 가능한 Component, 상태(Intance Variable), Getter, Setter, No-Args-Constroctor를 따로 저장해 둔 것이라고 한다. 즉, 오늘까지 이해한 바로는 계속 사용해야 할 것들을 콩속에 넣어두고 필요할 때마다 꺼내쓰도록 만든것이 bean이라는 것이다.

</div>
</details>
