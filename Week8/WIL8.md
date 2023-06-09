# WIL8

### **IoC와 프레임 워크, 라이브러리**

**IoC**는 inversion of Control의 약자로 **제어의 역전**이라는 뜻을 의미한다. IoC는 프로그램의 제어 흐름을 직접 제어하는 것이 아니라 외부에서 관리한다.

이때, 제어 흐름을 누가 하느냐에 따라 ‘프레임워크’인가 ‘라이브러리’인가로 구분되어질 수 있다.

즉, 개발자가 프레임워크에게 제어의 흐름을 넘겨주면, 프레임워크가 전체적인 흐름을 쥐고 있으며 애플리케이션의 코드는 프레임워크에 의해 조종되고, 반면 라이브러리는 개발자가 제어 흐름을 가지고 있으며 프로그램의 전체적인 흐름을 만들고 필요할 때마다 능동적으로 라이브러리를 호출하여 사용한다.

### **생성자를 통한 의존성 주입과 @Autowired 비교**

- **생성자를 통한 의존성 주입**
    - 생성자를 통해서 의존 관계를 주입받는 방법
    - 생성자 호출 시점에 딱 한 번만 호출되는 것이 보장
    - 불변, 필수 의존관계에 사용
    - 코드의 확장성과 유연성이 증가하는 장점이 있음
- **@Autowired 를 통한 의존성 주입**
    - 스프링 설정 파일을 보고 자동으로 속성의 설정자 메서드에 해당하는 역할을 함
    - Type 매칭을 시도하고, 여러 Bean이 존재할 경우( 같은 Type이 여러 개라면 ) **필드 이름**, **파라미터 이름**으로 빈 id을 추가 매칭

### **AOP**

: AOP는 Aspect-Oriented Programming의 약자로, 로직 주입을 의미

- 중복 코드, 프록시 클래스 작성의 번거로움 등 흔한 문제를 해결이 목적

- **스프링 AOP란?**
    - 스프링에서 제공하는 프록시 기반의 AOP 구현체
    - 스프링 빈에서 AOP 적용 가능
    - 메서드 실행 지점에만 AOP 적용 가능
- **특징**
    - 인터페이스 기반이다
    - 프록시 기반이다
        - 프록시 객체를 통해 스프링 빈에 부가 기능을 추가 가능
        - 프록시 객체는 기존의 타겟 객체를 참조
    - 런타임 기반이다

- 용어정리
    - **Aspect**  : 여러개의 Advice와 여러개의 Pointcut의 결합체. 즉, When + Where + What을 의미
    - **Advisor** : 한개의 Advice + 한 개의 Pointcut (1:1관계),  스프링 AOP에서만 사용됨
    - **Advice** : Pointcut에 적용할 로직, 메서드를 의미 ,Pointcut에 [언제(When), 무엇을(What)]를 을 적용할지 정의한 메서드
    특정 Join point에서 Aspect에 의해 취해지는 조치
    - **JoinPoint** : Aspect가 적용가능한 위치
    메서드 실행, 생성자 호출, 필드 값 접근, static 메서드 접근과 같이 프로그래밍 실행 중 지점
    - **Pointcut** :  횡단 관심사를 적용할 타킷 메서드를 선택하는 지시자 (메서드 선택 필터), “타킷클래스의 타깃 메서드 지정자”,  [어디에(where)]을 의미
    즉, Join point 중에서 Advice가 적용될 위치를 선별하는 기능을 함.