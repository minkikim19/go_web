 property와 value의 역할
  검색된 대상에 지정될 css명령

 inline
  html에 직접 css 작성

 embedder
  html style 안에 작성

 link
  link외부 문서 불러오는 방식


 @import
  외부 css문서 불러와 적용 (css파일에서 다른 css 가져옴)


selector
 기본 선택자
  
  전체 선택자
   (요소 내부의)모든 요소를 선택
   '*'

  태그 선택자
   html tag 선택


  클래스 선택자
   html에서 설정한 class 이름을 선택
   '.'

  아이디 선택자
   html에서 설정한 id를 선택
   '#'


복합 선택자
 
 일치 선택자
  동시에 만족하는 요소선택
  ex) span.orange(tag.class)

 자식 선택자
  자식요소 선택
  ex) ul > .orange

 후손 선택자
  후손 요소를 선택 (띄어쓰기로 구분)
  ex) div .orange

 인접 형제 선택자
  형제요소중 다음에 있는 하나를 선택(+로 구분)
  ex) .orange + li

 일반 형제 선택자
  형제요소중 다음에 있는 모두 선택 (~로 구분)
  ex) .orange ~ li


가상 클래스 선택자(pseudo-classes selectors)
  : 이렇게 사용

 hover 
  마우스가 올라가 있는 동안에만 선택
  ex) a:hover
 active
  마우스를 클릭하는 동안에만 실행
  ex) .box:active
 focus
  요소가 포커스 된 동안에만 실행(대화형 콘텐츠에서 사용가능 ex) input(요소를 선택했을 때 테두리선이 나타나는 것), img, tabindex)
  ex) input:focus

 first child
  형제 요소중 첫번째 요소라면 선택
  ex) .fruits li:first-child (fruits class중 li태그의 첫번째 요소)

 last child
  형제 요소중 마지막 요소라면 선택
  ex) .fruits li:last-child

 nth child
  형제 요소 중 n 번째 요소라면 선택(n 키워드 사용시 0부터 해석 (zero-base) )
  ex) .fruits li:nth-child(2) -> li의 2번째 요소 선택됨
      .fruits li:nth-child(2n) -> 짝수 번째 요소들만 선택 (2번째 4번째)
      .fruits li:nth-child(n+3) -> 3번째 요소부터 순차적으로 선택


 nth of type
  타입과 동일한 타입인 형제요소 중 n 번째 요소라면 선택 (zero base)
  ex) .fruits p:nth-of-type(1) -> 태그만 선택 가능하다 class는 선택 불가능 하다.

 부정 선택자(Negation selector) 
  ()안에 들어간 것이 선택되는게 아닌 왼쪽 끝에 있는게 실행됨
  ex) .fruits li:not(.strawberry) -> li태그안에 strawberry가 들어간 것만 빼겠다는 뜻







가상 요소 선택자(pseudo-elements selector)
  :: 을 이렇게 사용.
  
 before 
  요소 내부의 앞에, 내용을 삽입
  ex) ul li::before{ content: "숫자"; }
  output) 숫자1 숫자2 

 after
  요소 내부의 뒤에, content를 삽입
  ex) ul li::after{ content:"" }
      ul li::after{ content: url("") } -> 이미지 주소를 사용할 수 있다.

 특의점
  콜론을 하나만 사용하는것도 가능하다.



속성 선택자(attribute selectors)
 
 attr
  속성 포함한 요소 선택
  ex) [disabled] {  }

 attr=value
  속성을 포함하며 속성 값인 요소를 선택
  ex) [type="password"]{  } 

 attr^=value
  속성을 포함하며 속성 값으로 시작하는 요소 선택
  ex) [class^="btn-"] { } -> btn-으로 시작하는 class이름을 가진것들을 모두 포함

 attr$=value
  속성을 포함하며 속성 값으로 끝나는 요소 선택
  ex) [class$="success"] { }
      [class$="danger"] { }

 
상속 (inheritance)
  조상요소에 적용된css가 하위요소들에게도 적용됨
 
 상속되는 속성들
  font, color, text-align, text-indent, text-decoration, letter-spacing, opacity
  글자를 다루는 속성들

 강제 상속
  부모요소의 값을 자식요소의 값과 동기화시키는 법
   inherit 값 사용
   ex) .parent{ position: absolute; }  .child{ position: inherit; }



우선순위
 




-주의사항
 오른쪽에서 왼쪽으로 해석하기
 
 자식선택자와 후손선택자를 구분해서 쓰기.
 
 후손 선택자를 사용했을 경우 다른 행에 다른 코드를 더 집어넣는다면 그 행의 첫번째 줄도 인식되어 적용된다.

 ex) .box-group :first-child(이처럼 앞의 tag를 지워서 모든것을 포함한다 나타낼 수 있다.)



우선순위
 같은 요소가 여러 선언의 대상이 될 경우, 어떤 선언의 css 속성을 우선 적용할지 결정하는 방법
  1. 명시도 점수가 높은 선언이 우선 명시도
  2. 점수가 같은 경우, 가장 마지막에 해석되는 선언이 우선
  3. 명시도는 상속 규칙보다 우선
  4. !important가 적용된 선언 방식이 다른 모든 방식보다 우선

 1. 가장 중요 ( !important )
  모든 선언을 무시하고 가장 우선 
 
 2. 인라인 선언 방식(style attribute)
  인라인 선언
 
 3. 아이디(ID selector)
  아이디 선택자

 4. class selector
  클래스 선택자

 5. 태그
  태그 선택자

 6. 전체
  전체 선택자

 7. 상속
  상속 받은 속성은 항상 우선하지 않음 // 점수: 계산하지 않음


 :hover 처럼 '가상 클래스'는 '클래스' 선택자의 점수 (10pt)를 가지며 
 ::before처럼 '가상 요소'는 '태그'선택자의 점수 (1pt)를 갖는다.
 부정 선택자 :not()은 점수를 갖지 않는다.




css 단위  
 
 px 단위

 %단위
  부모에 영향을 받는다

 em
  현재 자신이 갖고 있는 폰트사이즈와 연관되어 있다.

 rem
  root em 
  html의 font size에 영향을 받는다.

 vw
  view with
  백분율 단위로 사용

 vh
  view hight
  백분율 단위로 사용

 vmin
  높이
  뷰포트 너비 또는 높이를 기준으로 하는 최소 값입니다.
  더 짧은 쪽의 백분율

 vmax
  너비
  뷰포트 너비 또는 높이를 기준으로 하는 최대 값입니다.
  더 넓은 쪽의 백분율

