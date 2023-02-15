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
    
#### 2023-01-11 Wed
1. 스프링 정석 Chapter2 쿠키와 세션에 대한 강의를 들었다.
    - 쿠키는 브라우저에서 생성하여 브라우저에 저장하고 서버와 주고 받는 데이터 모음이다.
    - 세션은 서버에서 생성하여 서버에 저장하고 전달받은 쿠키와 비교하여 사용하는 데이터 모음이다.
    
#### 2023-01-12 Thu
1. 스프링 정석 Chapter2 예외처리에 대한 강의를 들었다.
    - 예외처리를 처리하는 방법이 여러가지가 있다.
        1. try-catch
        2. 클래스 내에 @ExceptionHamdler를 이용한 처리 메서드 생성하기
        3. 새로운 클래스를 만들어 2에서와 같은 ExceptionHandler-method를 생성한다.
           이 때 @ControllerAdvice를 붙여주면 여러 클래스에서 발생하는 Exception을 한 번에 처리할 수 있다. 
            - @ControllerAdvice : 모든 클래스의 Exception을 처리
            - @ControllerAdvice("패키지 패스") : 특정 패스 내의 클래스에서 발생하는 Exception을 처리
        4. Error.jsp : 에러를 띄우는 view 파일을 만든뒤 속성에 isErrorPage="true"를 추가하면 자동으로 에러를 처리해준다.
        5. web.xml에 error-page 속성을 이용해 상태 코드별 띄울 view를 설정할 수 있다.
        6. servlet-context.xml에 SimpleMappingExceptionResolver를 추가해
            - View by Exception
            - Status code by View
           를 설정할 수 있다.
    
#### 2023-01-13 Fri
1. 스프링 정석 Chapter3 Spring으로 DB 연결하는 방법에 대한 강의를 들었다.
     - JDBC를 이용하는 방법과 Spring JDBC를 이용하는 방법
        - JDBC를 사용하면 DriveManager를 사용한다.
        - Spring JDBC를 사용하면 DriverManagerDataSource를 사용한다.
     - Spring JDBC : Bean에 연결 정보를 저장해 두고 사용할 수 있다.
2. 스프링 정석 Chapter3 Spring으로 DB (MySQL)을 다루면서 TDD사용을 배웠다.
     - 인스턴스 객체로 사용되는 DataSource 객체는 테스트 메서드들이 공유해서 사용하지 않는다.
     - 모든 테스트 들은 서로 독립적이어야 하고 실행 횟수에 상관없이 항상 성공해야 한다.
    
#### 2023-01-16 Mon
1. 스프링 정석 Chapter2 DispatcherServlet에 대한 강의를 들었다.
    - DispatcherServlet의 요청 처리 과정
        - 요청을 HandlerMapping에서 어떤 메서드로 처리할지 참조한다.
        - 처리할 메서드를 HandlerAdaptor를 통해 호출하고 결과로 Model과 출력에 사용할 View 이름을 받는다.
        - 이 View 이름을 이용해 ViewResolver에서 정확한 파일정보를 참조한다.
        - 여태까지 취합한 결과 Model,ViewFile 정보를 JstlView를 통해 Response 객체로 만들고 이를 Client로 보낸다.
    - DoDispatch
        - DispatcherServlet이 요청을 처리하는 일련의 과정을 처리하는 DispatcherServlet 내의 메서드이다.
    
#### 2023-01-17 Tue
1. 스프링의 정석 Chapter3 DAO에 대한 강의를 들었다.
    - DAO
        - Data Access Object
        - Table당 하나의 DAO가 존재한다.
        - DAO는 인터페이스로 구현하고 구현체는 DaoImpliment로 분리해서 구현한다.
    
#### 2023-01-21 Sat
1. 스프링 완전판 초격차 강의 Chapter1 Todo 리스트 만들기 강의를 들었다.
    - Modle, Repository, Serice, Controller를 한 번 빠르게 만들어보았다.
    - 빠르게 만들어 보니, Spring Boot로 웹을 구성하는 전체 그림을 그려볼 수 있어서 좋은 복습이었다.
    - RequestMapping("/") 하나를 이용해 GET, POST, PATCH, DELETE를 모두 활용하니 많은 기능을 Path 하나로 구현할 수 있었다.
    
#### 2023-01-25 Wed
1. 스프링의 정석 Chapter3 Transaction, Commit, Rollback에 대한 강의를 들었다.
    - Transaction : 더이상 나눌 수 없는 작업의 단위
    - Commit : 가공한 데이터를 DB에 반영하기
    - Rollback : 데이터 가공 중 직전 커밋상태로 되돌리기 (커밋을 잘못한 걸 알아챈 걸 되돌리는 것이 아니다.)
    - Transaction은 ACID를 따라야 한다.
        - Atomity : 원자성
        - Consistensy : 일관성
        - Isolation : 고립성
        - Durability
    - Isolation Level
        - Transaction은 독립적으로 수행되어야 하지만 DB의 성능 및 사용자의 편의를 위해 그 고립의 정도 (독립의 정도)를 조절할 수 있다.
            - READ UNCOMMITED : 커밋되지 않은 데이터도 읽을 수 있다. (고립도 최저)
            - READ COMMITED : 커밋된 데이터만 읽을 수 있다.
            - REPEATABLE READ : 자신의 Transaction이 시작 될 때의 데이터를 Transaction이 끝날 때까지 반복적으로 읽을 수 있다. 즉 Transacion이 진행중일 떄 반영된 DB의 데이터를 읽어들이지 않는다.
            - SERIALIZABLE : 한 번에 하나의 Transaction만 수행한다. 이론적으로 가장 이상적인 고립도이다. (고립되 최고)

#### 2023-01-26 Thu
1. 스프링의 정석 Chapter3 : AOP에 대한 강의 중 맛보기 부분만 들었다.
    - AOP는 동적으로 메서드에 코드를 삽입하는 기술이다.
    - 삽입할 코드를 분리시켜 작성한 클래스를 advice라 부른다.
    - 코드는 메서드의 맨 앞 또는 맨 뒤에만 삽입 가능하고 위치에 따른 명칭이 있다.
        - 맨 앞에 주입 : before-advice
        - 맨 뒤에 주입 : after-advice
        - 맨 앞과 맨 뒤 모두 주입 : around-advice
    
#### 2023-01-30 Mon
1. 스프링의 정석 Chapter3 : AOP와 @Trnasactional에 대해 공부중이다.
    - AOP = Asepct Oriented Programming = 관점 지향 프로그래밍
        - Cross-Cutting Concerns (= 횡단 관심사)를 분리하여 중복제거한다.
    - 분리한 코드를 실행하는 과정에서 동적으로 주입해주다. 이를 AOP라고 한다.
    - 용어
        - Advice : 부가기능로 분리해낸 코드를 말한다.
        - Target : Advice를 주입할 객체를 말한다.
        - Join Point : Target내에서 실제로 Advice가 주입될 대상(메서드)를 말한다.
        - Proxy : 동적으로 Advice가 Target내의 Join Point에 주입되어 마치 원래 하나의 객체였던 것처럼 보이는 순간의 객체를 Proxy라고 한다.
        - Weaving : Proxy를 만드는 과정을 Weaving이라고 한다.
        - Pointcut : join point를 특정하기 위해 정의한 패턴을 포인트 컷이라고 한다.
2. @Transactional
    - @Transactional 애너테이션이 붙은 Scope내의 모든 기능들이 성공적으로 수행됐을 경우에만 결과로 반영한다.
</div>
    </details>
    <details>
<summary>2023년 2월</summary>
<div markdown="1">       
#### 2023-02-02 Thu
1. 스프링의 정석 Chapter3 : Transaction 적용하는 실습을 했다.
    - TrnasacionManager
        - Tx를 적용하기 위해서는 TransactionManager 객체를 만들어야 한다.
        - TransactionManger를 이용해 TransactionStatus 객체에 Tx 정보를 담는다.
        - try-catch문에서 try 부분에 Tx로 묶을 일련의 과정 및 메서드들을 전부 담는다.
            - 모두가 성공적으로 이루어지면 TransactionManager를 이용해 TransactionStatus 객체를 Commit 한다.
            - 실패시 catch문이 받아서 TransactionManager를 이용해 TransactionStatus 객체를 Rollback 한다.
    - DataSourceUtils를 이용한 Connection 생성
        - Tx으로 묶여 있는 모든 메서드는 하나의 Connection을 공유해야 한다. 때문에 기존에 DataSource객체를 이용한 방식에서 DataSourceUtils를 활용한 Connection 생성 방식으로 변경해 줘야 한다.
    
#### 2023-02-08 Wed
1. 스프링의 정석 Chapter3 : @Transactional 완광했다.
    - @Transactional의 속성에 대해서 공부했다.
        - 그 중 Propagation에 대해서 알아봤다.
            - REQUIRED (Default) : 진행 중인 Tx의 요소로가 된다.
            - REQUIRES_NEW : 메인 Tx와 독립적인 Tx를 실행한다.
            - NESTED : REQUIRES_NEW와 동일하지만 메인 Tx가 Rollback시 함께 Rollback된다. 반대는 REQUIRES_NEW와 마찬가지로 성립하지 않는다.
            - SUPPORTS : 메인 Tx가 있다면 요소가 되지만, 없다면 Tx 수행 없이 진행한다.
            - MANDATORY : 메인 Tx 내에서만 작동하고 그렇지 않으면 예외를 발생한다.
            - NOT_SUPPORTED : Tx 적용 없이 실행하지만, 메인 Tx가 수행중이라면 일시정지(Suspend) 시킨다.
            - NEVER : Tx 적용 없이 실행하지만, 메인 Tx가 수행중이면 예외를 발생시킨다.
    
#### 2023-02-09 Thu
1. 스프링의 정석 Chapter4 : MyBatis 강의 듣기 시작했다.
    - MyBatis란
        - SQL Mapping Framework
            - SQL을 별도 XML 파일로 분리해 사용할 수 있도록 한다.
    

#### 2023-02-13 Mon
1. 스프링의 정석 Chapter4 : MyBatis 강의를 들었다.
    - MyBatis를 활용해 Mapper.xml을 작성하여 DAO를 작성했다.
        - Dao는 인터페이스로 구현한다.
        - DaoImpl로 Dao구현체를 구현한다. 이 때 실제 구현은 데이터를 DB에서 불러오고 반환하는 것은 Mapper.xml이 SQL문을 이용해 담당하고, DaoImpl은 Mapper에 있는 함수 select 등과 같은 태그를 호출하면서 필요한 인자를 전달하는 역할을 한다.
    
#### 2023-02-14 Tue
1. 스프링의 정석 Chapter4 : 페이징 공부
    
   
#### 2023-02-15 Wed
1. 스프링의 정석 Chapter4 : 게시판 만들기 공부중
    - 페이징, 목록으로 이동, 삭제 실습을 했다.
    
</div>
</details>
