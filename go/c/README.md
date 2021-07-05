html - 블록 레벨 요소와 인라인 요소

1. 블록요소
	1. div, h1, p
	2. 사용 가능한 최대 가로 너비를 사용한다.
	3. 크기를 지정할 수 있다.
	4. (width:100%; height:0;로 시작)
	5. 수직으로 쌓임
	6. margin, padding 위, 아래, 좌, 우 사용가능하다
	7. 레이아웃

2. 인라인 요소
	1. span, img
	2. 필요한 만큼의 너비를 사용한다.
	3. 크기를 지정할 수 없다.
	4. (width:0; height 0;로 시작)
	5. 수평으로 쌓임
	6. margin, padding 위, 아래는 사용을 할 수 없다.
	7. text



<meta name="author" content="test">
<meta name="description" content="test site">

인터넷 익스플로어에서 어떻게 표현될지에 관한 설명
<meta http-equiv="X-UA-Compatible" content="IE=edge">

경로를 기준으로 잡음 / title아래에 위치하는게 좋음. / 한번밖에 사용 못함 / 전역에 영향을 끼침
<base href="./css/">
<link rel="stylesheet" href="main.css">


<header></header>
<footer></footer>
html5는 의미를 가지는 tag를 사용

<h1>-<h6> 6단계의 문서 제목 구현
1. 제목폰트의 크기를 줄이기 위해 낮은 단계를 사용하면 안된다.
2. 제목단계를 건너뛰는 것을 하지 말아라 ex. 3. <h1>작성후<h3>작성하면 안된다. 순서대로 작성해라
4. 전체문서의 제목 h1 한번만 작성
5. 중복 제목은 h2를 사용


<main> body의 주요 컨텐츠
콘텐츠 구역은 문서의 핵심 주제나 애플리케이션의 핵심 가능성에 대해 부연, 또는 직접적으로 연관된 콘텐츠들로 이루어짐.

<article> 독립적으로 구분되거나 재사용 가능한 영역을 설정
<h1> <time datetime>

section - 문서의 일반적인 영역, 제목(h1~6)을 설정

aside - 문서의 별도 콘텐츠를 설정(보통 광고나 기타 링크 등의 side bar를 설정)

nav 다른 페이지 링크를 제공하는 영역
	navigation, 보통 메뉴, home, about, ontac, 목차, 색인 등을 설정


address body,article,footer등에서 연락처 정보를 제공하기 위해 포함하여 사용.

a href =" mailto: "
a href =" tel:+81010 "
이렇게 하면 os 화경 내의 application이 실행됨 (모바일 포함.ㅋㅋ)

div 본질적으로 아무것도 나타내지 않는 콘텐츠 영역을 설정
	꾸미는 목적으로 많이 사용됨





ol ul li
	ol 정렬 ul 정렬아님

dl dt dd
	용어(dt)와 정의(dd) 쌍들의 영역(dl)을 설정

p
	하나의 문단을 설정 (문장, 문단{단락})

hr /
	문단의 분리(주제에 의한)를 위해 설정.
	시각적 표현이 아닌 의미적 관점으로만 사용해야 한다.
	
	선이 아닌 사각형의 개념을 갖고 있기 때문에 border none 속성을 사용해서 없애준후 사용해야 한다.

pre
	서식이 미리 지정된 텍스트를 설정
	텍스트의 공백과 줄바꿈을 유지하여 표시할 수 있다.

blockquote
	일반적인 인용문을 설정
	cite 속성 url 값을 입력