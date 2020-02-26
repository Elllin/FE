# 이번주 배운 것

1. OOP WITH ES Classes

- OOP 핵심 개념
  - 캡슐화(Encapsulation)
  - 상속(Inheritance)
  - 다형성(polymorphism)
  - 추상화(abstraction)
- 좋은 OOP
- 역할과 책임
- 높은 응집도(high cohesion), 낮은 결합도(loose coupling)

2. JavaScript에서 객체나누기는 어떻게 해야할까?

- 보통 화면에 보이는 영역을 구분한 뒤에, 각각을 하나의 객체로 나누는 것이 좋다.

3. DOM제어

- node 탐색
- node 구조 변경

4. EVENT 종류 및 등록

5. ANIMATION

# [미션] 아마존 - 네비게이션UI

1. 아마존 네비게이션 UI 만들기

- HTML,CSS를 포함한다.
- ES6 Classes 를 사용한다.
- Classes 구현시 생성자의 인자를 잘 활용한다.
- Event 등록은 addEventListener를 사용한다.
- 모든 js코드의 실행은 DOMContentLoaded 이후에 실행한다.

2. 아마존 네비게이션 UI ANIMATION

- CSS transtion/transform을 사용한다.
- 자연스럽게 동작되도록 구현한다.
- 코드내에 매직넘버를 없앤다.

# 코드리뷰 받은 부분

1. 잘된 점

- 메서드들 이름은 구체적으로 잘 표현
- carousel 객체를 carouselCardMenu에 주입해줘서 의존성을 관리한 점,
  객체간의 관계가 코드에서 간단하게 보여지는 점
- 나눈 클래스의 역할과 동작방식이 괜찮음
- 클래스내의 메서드 크기가 적당

2. 개선할 사항

- 나눈 class의 Carousel의 역할과 CarouselSlider의 역할을 어떻게 정의한 것일까?
  함께 같이 있어도 될거 같다는 생각이 든다
  -> Carousel이 CarouselSlider와 CarouselCardMenu의 공통으로 사용하는 속성들로 묶어서 상위 개념의 class로 구현해보자 라는 생각으로 구현했지만 Carousel의 역활이 애매해졌다.
- constant라는 이름은 별로 의미가 없어 보여서 수정이 필요
- carousel도 뭘 지칭하는 건지 알 수 없다. 좀더 구체적인 네이밍 고민 필요
- 반복적인 코드 캐시해서 사용
- 객체 생성 시 객체리터럴 표현법을 활용

# 느낀점

class 나누는 것이 익숙치 않아 어려웠다. 크게 slider와 cardMenu 부분으로 나누려 했지만 slider class가 너무 무거워지는 것 같아 sliderBtn구현 부분을 다른 class로 분리했다. 클래스의 핵심 개념을 이해하는 것과 코드에 반영하는 것은 아직까지 못하고 있는 것 같다. 앞으로 class에 대한 이해가 좀 더 필요할 것 같다.
