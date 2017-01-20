5일차

- 애니메이션

keyframes로 각 구간 별 구현한 애니메이션 선언 후 

구현 할 곳에서 name,duration 속성으로 호출한 후 사용한다. 

다중 호출 가능 `div{animation-name: main-ani, sub-ani;}`

콤마(,)는 두 개 이상의 애니메이션을 동시에 적용할 때 사용.

연습 사이트: http://www.the-art-of-web.com/css/timing-function/

fill-mode: 애니 처음(backwards) / 끝(forwards)에서 머물게 하는 속성

name,duration외엔 적는 순서 상관없다.

visual 자식요소로 가상요소를 만들면 아래와 같이 span태그와 같은 위치에 생긴다.

```css
    <div class="visual">
      <span class="before"></span>
      <div class="visual-text">
        Web Standards &amp; Accessibility
      </div>
      <span class="after"></span>
    </div>
```



- 이미지명은 하이픈으로 적용할 경우 더 빠르게 인식한다.

- 멀티백그라운드 콤마(,)로 구분 단축표현은 중복사용 못함, 

  배경의 경우 나중에 선언한 것이 밑으로 온다.

- codepen 방문: steps animation 검색 후 첫 번째 예제



- 로그인 폼

버튼: form에서 정한 action으로 form에 담긴 정보를 보낸다.

마크업 후 tools 탭 / 파폭 35,36번 북마크에서 마크업 유효성 검사 해보기

- 입력서식 마크업 예시 잘된 사이트 https://miketaylr.com/pres/html5/forms2.html


- html pdf에 서식 list가 있음
- 논리속성이란? 태그에 =""없이 입력하면 true / 입력 안하면 false



- http://cssreference.io/ css 적용 모습을 코드작성 없이 볼 수 있음 - css속성 학습에 짱

- https://github.com/techhtml/html-best-practices/blob/master/README.md 

  조은님 HTML연습 

- 폴백칼라:그라디언트 안보일 경우 대체랑 배경화면 

  `background: #ff7512 radial-gradient(circle at right top, rgb(255, 224, 15), rgb(255, 46, 0));`

  위에선 `#ff7512`가 폴백칼라

  ​

