# 주차

---

**[목차]**

---

**[진행과정]** 

1. 크게 ‘필수 정리 내용’과 ‘강의내용’을 공부한 것을 기록
2. 공부하면서 개념이 추상적으로 다가오는 내용과 웹 개발에서 필요한 기초지식으로 모르는 개념이 많다고 느껴서 추가적인 공부가 필요한 부분을 중간중간에 기록함 ( 추후 내용 보충해보기 ) 
3. 강의들으면서 진행과정 따라하기 + 필수정리 내용에서 간단히 찾아보았던거 리마인드

# 필수 정리 내용

## MVC 패턴이란?

 : ‘**모델(Model), 뷰(View), 컨트롤러(Controller)‘**로 이루어진 디자인 패턴

<aside>
💡 **여기서 잠깐 !! 디자인 패턴**은 뭐야?

**디자인 패턴**이란 프로그램을 설계할 때 발생했던 문제점들을 객체 간의 상호 관계 등을 이용하여 해결할 수 있도록 ‘**하나의 규약 형태’** 로 만들어 놓은 것

**추가공부!** 디자인 패턴의 종류에는 싱글톤, 팩토리, 전략, 옵저버, 프록시 패턴 등 많은 패턴들이 있으니 따로 공부해보도록 하자!

</aside>

:  MVC 패턴은 애플리케이션의 구성 요소를 **세가지 역할**로 구분하여 개발 프로세스에서 각각의 구성요소에만 집중해서 개발할 수 있다

: **재사용성과 확장성이 용이**하다는 장점과, 애플리케이션이 복잡해질수록 **모델과 뷰의 관계가 복잡**해지는 단점이 있다.

> **컨트롤러 (Controller)**
> 

: 하나 이상의 모델과 하나 이상의 뷰를 잇는 **다리** 역할

- 모델과 뷰의 **생명주기 관리**와 **메인 로직** (이벤트 등)을 담당
- 모델이나 뷰의 변경통지를 받으면 이를 해석하여 각각의 구성요소에 해당 내용에 대해 알려줌

> **모델 (Model)**
> 

: 애플리케이션의 데이터인 **데이터베이스, 상수, 변수** 등을 뜻함

- 뷰(View)에서 데이터를 생성 / 수정하면 컨트롤러(Controller)를 통해 모델을 생성하거나 갱신함

ex. 사각형 모양의 박스 안에 글자가 들어있다면 그 사각형 모양의 박스 위치 정보, 글자 내용, 글자 위치, 글자 포맷(utf-8 등)에 관한 정보를 모두 가지고 있어야 한다.

> **뷰 (View)**
> 

: 모델을 기반으로 **사용자가 볼 수 있는 화면**을 뜻함

- **사용자 인터페이스 요소**( inputbox, checkbox, textarea 등 )을 나타냄. ex. 단순히 사각형 모양
- 모델이 가지고 있는 정보를 저장하지 않아야 하며, 변경이 일어나면 컨트롤러에 전달해야 함.

---

특히, API 와 RESTAPI 개념들을 찾아보니 기초지식이 많이 부족함을 느꼈다. 밑에 내용부분은 꼭 더 공부해서 다시 보자~!

<aside>
💡 **기초지식** **추가공부필요 ! 
1. HTTP란 무엇인가?
2. URL**

</aside>

- **HTTP ( 진행중 )**
    
    ## HTTP란?
    
    웹 환경에서 서버와 클라이언트가 어떻게 데이터를 주고받을지 정해 놓은 규칙 서버 간에 데이터를 주고 받을 때도 대부분 HTTP를 사용한다.
    거의 모든 형태의 데이터 전송 가능
    HTML, TEXT / 이미지, 음성, 영상, 파일 / JSON, XML 등
    
    HTTP 주요 버전 
    
    HTTP에도 버전이 있다 . 주요 버전으로는 HTTP/1.1, HTTP/2  HTTP/3 이 있다.
    
    현재 HTTP/1.1을 주로 사용하고 있으며, 2와 3도 증가하는 추세
    
    ## HTTP 주요 특징
    
    ### 1. 클라이언트 , 서버 구조
    
    HTTP는 클라이언트, 서버 구조로 되어 있다. Requestk Respense 구조
    
    ### 2. 무상태(Stateless) 프로토콜
    
    - **상태 유지 (Stateful)**
    
    서버가 클라이언트의 정보를 계속 가지고 있음
    
    클라이언트 정보를 가진 서버 외에는 정확한 응답 메세지를 주기 어렵다
    
    **서버의 확장성이 떨어진다**
    
    서버는 우리 상태를 항상 기억하고 있다고 가정하고 요청을 보냄
    
    - **무상태 (Stateless)**
    
    서버가 클라이언트의 정보를 가지고 있지 않음
    
    클라이언트가 서버가 필요한 정보를 그때마다 모두 보냄
    
    클라이언트 요청에 어느서버든 응답할 수 있다
    
    **서버의 확장성이 높다 ( 무한한 서버 증설 가능 )** 
    
    ### 3. HTTP 메세지 구조
    
    HTTP 메세지 구조는 **시작 라인, 헤더, 공백, 바디**로 나뉜다.
    
    - http 요청 메세지 구조
    
    시작 라인 : http 메서드 , 요청 대상 (path) , 
    
    - 참고자료
        
        [HTTP 기본](https://loopstudy.tistory.com/322?category=1031527)
        
    
- **URI** vs **URL** vs **URN ( 진행중 )**
    
    [URI URL URN이란 무엇인가? (REST API를 공부하기 위하여)](https://backhero.tistory.com/7)
    
    [URI와 웹 브라우저 요청 흐름](https://loopstudy.tistory.com/321)
    

## API(Application Programing Interface)

: Application Programming Interface의 준말로 여러 프로그램들과 데이터베이스, 그리고 기능들의 **상호 통신 방법을 규정**하고 도와주는 ***인터페이스**이다. 즉, 액세스 권한이 있는 앱의 권한 규정과 서비스 요청에 따라 데이터나 서비스 기능을 제공하는 메신저 역할을 

서버는 클라이언트에게 회원가입을 시키는 API를 URL 형태로 제공

클라이언트는 서버에서 무슨 로직으로 회원가입을 동작시키는지 전혀 모른다

*인터페이스 : 서로 다른 2개의 요소에서 신호를 주고 접점

---

## RESTful API는 뭐야?

### **REST?**

:  Representational State Transfer의 준말로, 리소스를 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것을 의미

- HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시
- HTTP Method(POST, GET, PUT, DELETE, PATCH 등)를 통해
- 해당 자원(URI)에 대한 CRUD Operation을 적용

### RESTful API

: HTTP 요청을 보낼 때, **메서드 + URL 형태**로 개발자들 사이에 널리 지켜지는 약속

- 각 요청이 어떤 동작이나 정보를 위한 것인지를 **요청 자체로 추측가능**
- **메서드**는 **행위**(동사)를 나타내며, **URL**은 **리소스**(명사)를 나타냄
- REST API는 3가지구성 요소를 가진다
    - **자원**(RESOURCE) - URI
    - **행위**(Verb) - HTTP METHOD
    - **표현**(Representations)

<aside>
💡 **기초지식** **추가공부필요 ! 
 HTTP 메서드란 무엇인가?**

</aside>

- 참고자료
    
    [REST API - URL Naming Conventions](https://restfulapi.net/resource-naming/)
    
    [[Network] REST란? REST API란? RESTful이란?](https://velog.io/@seokkitdo/Network-REST%EB%9E%80-REST-API%EB%9E%80-RESTful%EC%9D%B4%EB%9E%80)
    
    [[Network] REST란? REST API란? RESTful이란? - Heee's Development Blog](https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html)
    
    [https://loopstudy.tistory.com/322?category=1031527](https://loopstudy.tistory.com/322?category=1031527)
    
    [REST API URI 규칙](https://velog.io/@pjh612/REST-API-URI-%EA%B7%9C%EC%B9%99)
    
    [[REST API] HTTP Method PUT vs PATCH](https://velog.io/@insutance/REST-API-HTTP-Method-PUT-vs-PATCH)
    
    [HTTP 메소드 PUT , PATCH 차이 - 삽질중인 개발자](https://programmer93.tistory.com/39)
    
    [[번역] Path Variable과 Query Parameter는 언제 사용해야 할까?](https://ryan-han.com/post/translated/pathvariable_queryparam/)
    
    [REST API 제대로 알고 사용하기 : NHN Cloud Meetup](https://meetup.nhncloud.com/posts/92)
    
    [REST API 이해와 설계 - #2 API 설계 가이드](https://bcho.tistory.com/954)
    

# 스프링 입문 강의

## 프로젝트 생성

### Spring initailizr 로 스프링 프로젝트 생성

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled.png)

Maven & Gradle : 필요한 라이브러리를 땡겨서 오고 빌드하는 라이프 사이클까지 관리해주는 툴 

Dependencies : 스프링 부트 기반으로 프로젝트를 시작할때 어떤 라이브러리를 땡겨쓸지 정함 + html 을 만들어주는 템플릿 엔진  ( thymeleaf )

### 📁src 폴더 : main과 test 폴더 두가지로 구분

- 📁main : 자바와 resources 파일 존재 ( resources는 실제 자바 코드 파일을 제외한 설정파일, xml 등이 들어가있음 ⇒ java 파일을 제외한 파일들이 들어가있다고 봐도 무방 )
    - 📁java : 실제 패킷이랑 소스파일 존재
    - 📁resources : 실제 java 코드파일 제외한 xml, html, 설정파일 등이 들어있음
- 📁test : test코드들과 관련된 소스들이 들어있다

![스크린샷 2023-01-13 오후 1.49.26.png](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-01-13_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_1.49.26.png)

<aside>
💡 **추가공부 !** **test 코드란? 무엇인지 알아보자**

</aside>

 

### 📁build.gradle 폴더

: spring initializr로 생성한 version 설정들과 라이브러리들( thymeleaf, web ) 등을 보여줌

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%201.png)

 

### 📁HelloSpringApplicaion 폴더

: main 메소드 실행화면 & 웹브라우저에 에러메세지로 동작확인(http:// [localhost](http://localhost):8080 ) 

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%202.png)

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%203.png)

---

## 스프링부트 핵심 라이브러리 살펴보기

: 빌드 tool (Maven, Gradle )들은 의존관계를 관리해준다 ⇒ 필요한 라이브러리들을 다 땡겨옴

### 📊spri**ng-boot-starter-web**

- spring-boot-starter-tomcat : 톰캣 (웹서버 : 8080)
- spring-webmvc : 스프링 웹 MVC

### 📊**spring-boot-starter-thymeleaf: 타임리프 템플릿 엔진(View)**

### 📊**spring-boot-starter(공통): 스프링 부트 + 스프링 코어 + 로깅 라이브러리 모두를 포함**

- spring-boot
    - spring-core

### 📊**spring-boot-starter-logging**

: 현업에서는 출력을 log로 해야한다

- logback : 실제 로그를 어떤 구현체로 출력할지
- slf4j : 인터페이스 역할

### 📊**spring-boot-starter-test :테스트 라이브러리**

- junit: 테스트 프레임워크
- mockito: 목 라이브러리
- assertj: 테스트 코드를 좀 더 편하게 작성하게 도와주는 라이브러리
- spring-test: 스프링 통합 테스트 지원

---

## View 환경설정

**static/index.html : static 폴더 하위에 index.html 파일 추가**

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%204.png)

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%205.png)

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%206.png)

**thymeleaf 템플릿 엔진**

main>java>hello.hellospring 하위에 controller 패키지 추가 → HelloController 자바파일 추

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%207.png)

templates폴더 하위에hello.html파일추가

![Untitled](%E1%84%8C%E1%85%AE%E1%84%8E%E1%85%A1%20404aaa0605b04e3cbae31338413b355e/Untitled%208.png)

---

## 빌드하고 실행하기

서버에 배포할때는 .jar파일만 복사해서 서버에 넣어주고 실행시켜주면 서버에 스프링이 실행됨.

---

## 정적 컨텐츠

: 말그대로 ‘변화가 없는 컨텐츠’를 의미, 개발에서는 서버에서 파일을 그대로 웹브라우저에 내려주는 것을 말함. 보통 HTML, CSS, JS와 같이 미리 서버에 저장해두고 서버가 요청을 받으면 그저 응답만 해주면 되는 것들로 구성됨

<aside>
💡 **추가공부 !** 웹 어플리케이션이 동작하는데 ‘**동적 컨텐츠**’와 ‘**동적 + 정적**’ 도 사용하던데 한번 알아보자

</aside>

---

## MVC와 템플릿 엔진

<aside>
💡 **추가공부 !** **템플릿 엔진**이 정확히 무엇이고 종류는 어떤게 있나

</aside>

- jsp, php 등 템플릿 엔진을 사용

- 서버에서 프로그래밍 해서 html을 동적으로 바꿔서 내리는 것

- Model, View, Controller

- 정적 컨텐츠와의 차이는 서버에서 html을 무언가 바꿔서 내린다는 것

---

## API

- 안드로이드나 아이폰 클라이언트와 개발할때는 JSON형태로 정보를 전달하는데 이런 방식을 API 방식이라 한다.

- Vue.js나 React도 API 방식으로 많이 사용

- 서버끼리 통신할 때도 API 방식으로 사용

서버에 배포할때는 .jar파일만 복사해서 서버에 넣어주고 실행시켜주면 서버에 스프링이 실행됨.