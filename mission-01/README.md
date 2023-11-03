# homework - 01

---

#### 프론트엔드스쿨 8기

#### 회고1조 손삼열

##### 과제: 주어진 Figma파일의 UI를 참고하여 HTML, CSS파일을 작성하기

---

1. **HTML 마크업**

- 이미지에서 보이는 것과 같이 총 3개의 섹터를 &lt;section&gt;태그로 나눠준다.
- 각각의 &lt;section&gt;은 로고, 텍스트, 이미지가 들어가는 동일한 패턴을 가지고있다.
- 로고와 이미지는 &lt;img&gt;, 텍스트는 &lt;h1&gt;, 버튼은 &lt;button&gt;로 마크업한다.
- **이 때, section-02의 button은 > 요소를 추가해야 하기 때문에 하위 항목으로 img태그를 포함시킨다.**
- **section-02와 section-03은 flex 속성을 이용해 배치할 예정이니 div태그로 감싸준다.**
  <br>

2. **CSS 스타일링 작업**

- **section 구조 잡기**

  - flex를 이용해 3개의 section의 구조를 잡기로 하자.
  - section의 부모요소인 body에 flex 속성을 부여한다.
  - flex의 흐름은 column 방향이니 flex-direction은 column을 부여한다.
  - **section-02와 section-03은 요소 두 개가 한 열에 배치되어야 하기 때문에 컨테이너 요소에 flex속성을 부여한다**
  - 이 때, flex의 흐름은 row 방향이므로 flex-flow에 row와 nowrap속성을 부여한다.
  - 컨테이너에 위 쪽으로 margin을 만들어 section-01과 일정한 거리를 둔다.
  - section-02와 section-03 사이의 거리를 두기 위해 각각 좌우 여백을 만들어준다.
    <br>

- **section 내부 아이템 배치하기**

  - 각 section의 하위 요소들은 section의 위치를 기반으로 position 할 예정이기 때문에 **section에 position:relative 속성을 부여한다.**
  - 그리고 **각 하위 요소들의 position은 absolute로 설정해준다.**
  - 각 요소들의 width와 height, 좌표를 확인하여 알맞게 배치시켜준다.

  <br>

- **h1태그 중앙정렬**
  - h1태그는 agent style로 상하여백이 포함되어있다.
  - h1태그에 margin을 제거해준다.
  - section-01의 경우 **h1에 text-align: center, line-height를 height와 일치시켜주는 것**으로 수평,수직 중앙정렬해준다.
  - section-02와 section-03의 경우 수평정렬은 동일하게,수직정렬은 **flex의 영향을 받고 있기 때문에 flex-shrink를 이용하여 수행한다.**

<br>

- **버튼 스타일링**
  - button-01, button-03은 background-image를 할당해주는 것으로 간단하게 버튼을 만들어 줄 수 있다.
  - button-02는 **display 방식을 inline-flex로 만들어 flex 방식으로 중앙정렬을 해준다.**
