## 의존성 주입
- 컨테이너가 연관 관계를 직접 규정하는 것
- 코드가 연관관계를 정의하지 않음
  - xml형식의 spirng di config을 사용해 의존성 관리
  - @형식의 어노테이션을 사용해 의존성 관리

## 강한 결합과 약한 결합
- 각각의 독립적인 기능간 의존성을 분리하여 프로그램이 변경에 강하도록 설계
- 서로 관련이 있는 기능은 강하게 결합 ( tightly )
- 서로 관련이 없는 기능은 약하게 결합 ( loosely )


## 의존성 주입의 장점
- 클래스들 간의 의존 관계를 최소화
- 어플리케이션의 유지 및 관리가 편리
- 객체의 생성과 소멸을 컨테이너가 자동 관리함


## 제어 역전
- 객체를 다루는 주체가 개빌자에서 프레임워크로 변경됨을 의미
- Spring 프레임워크에서는 Spring이 직접 객체의 생성과 소멸을 관리
- IoC의 종류는 여러가지가 있으며 DI는 IoC를 구현하는 여러 방법들 중 하나임
  - DL : 컨테이너 저장소에 저장되어 있는 Bean에 접근하기 위해 컨테이너가 제공하는 API를 이용하여 bean을 Lookup 하는 것
  - DI : 각 클래스간 의존관계를 빈 설정 정보를 바탕으로 커넽이너가 자동으로 연결해주는 것
    - Setter Injection : 의존성을 입력 받는 setter메서드를 만들고 이를 이용해 의존성을 주입
    - Constructor Injection : 필요한 의존성을 포함하는 클래스의 생성자를 만들고 이를 통해 의존성을 주입
    - Method Injection : 의존성을 입력받는 일반 메서드를 만들고 이를 통해 의존성을 주입


## Bean 태그에 사용되는 속성
- id : 빈 객체의 고유 이름, 이를 사용해 빈에 접근
- name : 객체의 별칭
- class : 생성할 클래스. 패키지 이름까지 입력 필요
- constructor-arg : 생성자를 이용한 의존성 주입
- property : setter를 이용한 의존성 주입
- lazy-init : 빈 생성 시점을 lazy하게 설정