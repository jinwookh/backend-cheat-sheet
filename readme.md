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
- BigInteger, BigDecimal, Date, Calendar, Date, Time 등 다양한 자료형을 사용할 수 있다.

## spring
- spring은 lightweight Container와 연관이 있다.
- lightweight Container의 특징
  - 컨테이너가 오브젝트의 생명주기를 관리한다.
  - 컨테이너를 통해 오브젝트에 접근할 수 있어야 한다.
  - 컨테이너를 통해 오브젝트를 관리할 수 있어야 한다.(configure)
  - 컨테이너는 dependency를 관리할 수 있어야 한다.
BeanFactory, ApplicationContext, Component, Service, Configuration, Bean, SpringBootApplication
