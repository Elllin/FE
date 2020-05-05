## 이번주 배운 것

- 비동기프로그래밍
  - call stack, callback queue,  event loop
- fetch API
- Promise 패턴
- Ajax
- DOM-TEMPLATING

## [미션] 아마존 - 비동기통신

1. JSON만들기

- 카드UI 기획에 필요한 데이터를 JSON형태로 만들어본다.
- 카드 데이터별로 유니크한 id, Title, desc, imgURL 등을 포함시킨다.
- localData.json 으로 저장한다.

2. fetch API 적용

- 로컬서버 환경을 구성한다. (ex. http://localhost:8080/amazon.html)
- 로딩이 완료되는 시점에, fetch API 를 활용해서 요청/응답을 받는다.
- 응답결과로 화면에 업데이트되야 한다. template literal 문법을 활용한다.
- 한번 가져온 데이터는 local storage에 cache해서 재사용한다. 즉,  한번 요청한 정보는 다시 요청하지 않음
- 함수의 역할을 고민하고, 가급적 작은 함수로 분리해서 개발한다.

## 코드 개선사항

- class별로 파일 분리
- className등 속성들을 config파일로 분리
- event 콜백함수를 분리
- 클래스 생성시 객체 리터럴 활용

## 코드리뷰

1. class는 네이밍을 어떻게 해야 할까 하는 고민

- 보통 너무 구체적이지 않는 명사로 표현
    예 > 바리스타클래스, 점원클래스, 커피메이커클래스

2. 잘된 점

- main소스 구성 잘됨
- 클래스 크기 적당하다
- bind 사용 동작에 대해서 설명하실 수 있어야한다
- 전체적으로 이름은 잘 지었다

  3. 개선할 사항

- this.selectorName의 이름은 문자열 같기 때문에 (하지만 객체임) this. selector등의 이름으로 수정하는게 더 좋을 것 같다
- util함수의 이름은 $보단 _$으로 =>
    \$가 jquery라이브러리로 생각하기 때문

```js
this.setCardBtnIndex();
cardBtns.forEach((btn, index) => {
  btn.addEventListener("click", () => {
    this.slider.slideIndex = index + 1;
    this.addScaleEffect(btn);
    this.slider.addTransition();
  });
});
```

- 위 코드는 이번주 델리게이션 공부 후 개선하기

## 느낀점

저번 주에는 Carousel의 기능이라는 작은 부분만을 구현했지만 이번 주는 fetch를 받고 template 작업도 해줘야 했기 때문에 나눈 class와 파일들을 어떻게 조립하고 작동시켜야 할지가 너무 어려웠다. 다른 사람의 코드를 보며 코드 조립? 하는 방법을 배워야겠다고 느꼈다.

## demo
[데모](https://elllin.github.io/demo/amazon-search/)
