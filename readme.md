# backend cheat sheet

## jpa
- hibernate가 jpa보다 더 먼저 나옴
- jpa는 @Entity를 써야 한다.
- no argument constructor는 필수다.
- class, method 모두 final로 선언되면 안 된다.
- 인스턴스 변수는 private, protected, package-private 중 하나여야 한다.(public이면 안 된다)
- @Transient를 사용하면 db와 상관없이 필드를 정의할 수 있다.
- Collection을 사용할 거라면 List, set, map 중 하나만 사용한다.
- 모든 entity는 primary key가 있어야 한다.
- BigInteger, BigDecimal, Date, Calendar, Time 등 다양한 자료형을 사용할 수 있다.
- (BigInteger, BigDecimal) -> decimal, (Date, Calendar) -> datetime, Time -> time 으로 변환된다.

## spring
- spring은 lightweight Container와 연관이 있다.
- lightweight Container의 특징
  - 컨테이너가 오브젝트의 생명주기를 관리한다.
  - 컨테이너를 통해 오브젝트에 접근할 수 있어야 한다.
  - 컨테이너를 통해 오브젝트를 관리할 수 있어야 한다.(configure)
  - 컨테이너는 dependency를 관리할 수 있어야 한다.
- BeanFactory, ApplicationContext, Component, Service, Configuration, Bean, SpringBootApplication

## java
- jvm: 자바 바이트 코드를 os 특화 코드로(어셈블리?) 변환한다.
- jvm 속 인터프리터: 바이트 코드를 한 줄씩 실행한다.
- jvm 속 jit 컴파일러: 반복되는 코드를 모두 os 특화 코드로 미리 바꾼다.
- spring dependency injection, mvc view로 넘어온 데이터를 객체로 만들 때 reflection을 사용한다.
- byte조작: 메모리에 올라가기 전에 바이트코드를 조작하는 기술 ex) pinpoint, 코드 커버리지 계산
- reflection: 이미 메모리에 올라간 클래스 정보 얻어오기 ex) 스프링 의존성 주입
- dynamic proxy: 새로운 클래스를 런타임에 생성 ex) Mockito
- annotation processor: 새로운 클래스를 컴파일 타임에 생성 ex) lombok
