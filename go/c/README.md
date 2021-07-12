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

a
	download / href / hreflang / rel / target / type
	<a href="./README.md" download>README.md</a> 이렇게 되어 있을경우 readme를 클릭하면 파일이 다운로드 된다. / 그냥 작성했을 경우 새로운 탭에 열린다

	다른 페이지, 같은 페이지 위치(#, 해시 태그), 파일, 이메일 주소, 전화번호 등 다른 url로 연결할 수 있는 하이퍼링크를 설정.

	* 같은 페이지 내에서 이동
	<a href="#title1"> title1 </a> 
	<h2 id="title1"> title1 </h2>


abbr
	약어를 지정 (abbreviation) / title 속성 사용

b
	문체가 다른 글자의 범위를 설정
	읽기 흐름에 도움을 주는 용도로 사용 (css를 사용할 수 없을 때 사용)

mark
	사용자의 관심을 끌기 위한 하이라이팅할 때 사용 (css를 사용할 수 없을 때 사용)

em
	단순한 의미 강조를 표시 / 중첩이 가능(중첩될 수록 강조 의미가 강해짐) / 기본적으로 이탤릭체로 표시됨

strong
	의미의 중요성을 나타내기 위해 사용 / 기본적으로 bold 표시

i
	위에서 나온 태그중 적합한 의미가 아닌 경우 사용(아이콘이나 특수기호를 사용할 때)


dfn
	용어를 정의할 때 사용(definition)

cite
	창작물에 대한 참조를 설정 (책, 논문, 영화, tv프로그램, 노래, 게임등의 제목) / 기본적으로 italic type으로 표시됨.

q
	짧은 인용문을 설정 (inline quotation) / 긴 인용문일경우 blockquote를 사용. / cite 속성 (인용된 정보의 url)

u
	밑줄이 있는 글자를 설정 (하지만 css로 커버가능)

code
	컴퓨터 코드 범위를 설정(inline code) / monospace글꼴 계열로 표시됨

kdb
	텍스트 입력 장치(키보드)에서 사용자 입력을 나타내는 텍스트 범위를 설정 (keyboard input)

sup, sub
	위 첨자(sup), 아래 첨자(sub)

time
	날짜나 시간을 나타내기 위한 목적으로 사용 / ie에서 사용불가

span
	본질적으로 아무것도 나타내지 않는 콘텐츠 영역을 설정

br /
	줄바꿈을 설정 / 간격을 만들어내는 용도로 사용해서는 절대 안된다.

del
	삭제된(변경된) 텍스트의 범위를 지정 / cite, datetime 속성을 사용
ins
	새로 추가된(변경된) 텍스트의 범위를 지정 / cite, datetime 속성을 사용

# tag가 가지는 의미에 집중하자

img
	width든 height든 px단위가 아닌 숫자로만 가로와세로 사이즈를 같이 변경할 수 있다.
				고정된 이미지 사용할 때
				width = "400"
				해상도가 변경됨에 따라 고정된 이미지의 해상도를 바꿀 수 있디.

	srcset - 브라우저에게 제시할 이미지 url과 원본 크기의 목록의 정의
				px 단위가 아닌 w 단위(이미지의 원본 크기 '가로 너비') 혹은 x 단위(이미지의 비율, 의도 <일반적으로 w사용> )를 입력, 작은 크기 이미지부터 순서대로 입력
	
	sizes - 미디어 조건과 해당 조건일 때 이미지 '최적화' 크기의 목록을 정의
				최적화 할 때 사용.
				sizes = "(min-width: 1000px) 700px " 가로가 1000px이 넘었을 경우 700px 사용

	width는 이미지의 출력크기
	sizes는 이미지의 출력 크기 + 최적 크기

audio
	autoplay - 준비되면 바로 재생
	controls - 제어 메뉴를 표시
	loop - 재생이 끝나면 다시 처음부터 재생
	preload - 페이지가 로드될 때 파일을 로드할지의 지정(힌트 제공)
	src - 콘텐츠 url
	muted - 음소거 여부


video
	동영상 콘텐츠(.mp4)를 삽입
	autoplay - 준비되면 바로 재생
	controls - 제어 메뉴를 표시
	crossorigin - 가져 오기가 CORS를 사용하여 수행되어야하는지 여부
	loop
	muted
	poster - 동영상 섬네일 이미지 url
	preload - (위와 동일)
	src - 콘텐츠 url
	width - 동영상 가로 너비
	height - 동영상 세로 너비

 figure
	이미지나 삽화, 도표 등의 영역을 설정
	이미지와 설명을 쓰고 싶을 때

	figure
		img src = " "
		figcaption ~에 관한 이미지 입니다. /figcaption 
	/figure

 figcaption
	figure에 포함되어 이미지나 삽화 등의 설명을 표시



iframe
	다른 html 페이지를 현재 페이지에 삽입
	src - 포함할 문서의 url
	width
	height
	style
	allowfullscreen - 전체 화면 모드 사용 여부
	frameborder - 프레임 테두리 사용 여부
	sandbox - 보안을 위한 읽기 전용으로 삽입


canvas
	canvas api이나 webgl api를 사용하여 그래픽이나 애니메이션을 랜더링.
	(픽셀단위는 적지 않아도 됨. 자바스크립트를 사용해야함.)
	width
	height

script
	스크립트 코드를 문서에 포함하거나 참조.(외부 스크립트)
	async - 스크립트의 비동기적(asynchronously) 실행 여부 //순차적 - 동기, 비순차적 - 비동기
	crossorigin - 
	defer - 문서 파싱(구문 분석) 후 작동 여부
		스크립트 파일의 위치에 따라서 작동이 제대로 되는 경우와 아닌 경우가 있다.
		하지만 이 속성을 사용하면 html파일을 전체적으로 실행후 자바를 실행하기 때문에 괜찮다.

	src - 참조할 외부 스크립트 url // 포함된 스크립트 코드는 무시됨(src로 스크립트를 불러왔을때 기존에 작성되었던 스크립트는 무시되어 실행되지 않는다.)
	type - text/javascript'


noscript
	자바 스크립트가 실행되지 않는 환경에서 표시되는 html을 정의





테이블

 table tr th td
	데이터 표<table>의 행<tr> 열<th><td> 을 생성

 th
	머리글 칸을 지정
	abbr - 열에 대한 간단한 설명
	headers - 관련된 하나 이상의 다른 머리글 칸 id 속성 값
	colspan - 확장하려는 열의 수
	rowspan - 확장하려는 행의 수
	scope - 자신이 누구의 머리글 칸인지 명시
 
 td
	일반 칸을 지정
	headers - 관련된 하나 이상의 다른 머리글 칸 id 속성 값
	colspan 확장하려는 열의 수
	rowspan 확장하려는 행의 수

 caption
	표의 제목을 설정
	열리는 table 태그 바로 다음에 작성해야 함.
	table 당 하나의 caption만 사용 가능

 colgroup col
	표의 열들을 공통적으로 정의하는 컬럼<col>과 그의 집합 <colgroup>
	col 부분에만 style을 적용시키고 싶을 떄 사용한다.
	span - 연속되는 열 수(그 옆 줄도 적용 시킬 수 있다)

 thead tbody tfoot
	표의 머리글<thead> 본문<tbody> 바닥글<tfoot>을 지정


양식
 form
	웹 서버에 정보를 제출하기 위한 양식 범위를 정의
	*action - 전송한 정보를 처리할 웹페이지의 url
	autocomplete - 사용자가 이전에 입력한 값으로 자동 완성 기능을 사용할 것인지 여부
	* method - 서버로 전송할 http 방식
	* name - 고유한 양식의 이름
	novaildate - 서버로 전송시 양식 데이터의 유효성을 검사하지 않도록 지정
	target - 서버로 전송 후 응답받을 방식을 지정

 input /
	사용자에게 입력 받을 데이터 양식
	autocomplete
	autofocus - 페이지가 로드될 때 자동으로 포커스
	checked - 양식이 선택되었음을 표시
	disabled - 양식을 비활성화
	form - form의 id속성 값
	list - 참조할 datalist의 id속성 값
	max - 지정 가능한 최대 값
	min - 지정 가능한 최소 값
	maxlength - 입력 가능한 최대 문자 수
	muliple - 둘 이상의 값을 입력 할 수 있는지 여부(여러개의 파일을 입력받을 경우)
	* name - 양식의 이름
	placeholder - 사용자가 입력할 값의 힌트
	readonly - 수정 불가한 읽기 전용
	step - 유효한 증감 숫자의 간격
	src - 이미지의 url
	alt - 이미지의 대체 텍스트
	* type - 입력 받을 데이터의 종류
	* value - 양식의 초기 값

데이터 type의 value
	button - 일반 버튼
	checkbox - 
	color
	email
	file
	hidden
	image - 제출버튼으로 활용해서 클릭할 수 있다.
	number
	password
	radio
	range
	reset
	search
	submit
	tel
	text
	url


 label
	라벨 가능 요소의 제목
	for 속성으로 라벨 가능 요소를 참조하거나 콘텐츠로 포함
	라벨 가능 요소 button input progress select textarea
	텍스트를 눌러도 체크됨

 button
	선택 가능한 버튼을 지정
	autofocus
	disabled
	form - form 의 id연결
	name - 폼 데이터와 함께 전송되는 버튼의 이름
	type - button, reset, submit

 textarea
	여러 줄의 일반 텍스트 양식
	rows - 양식의 줄 수

 fieldset legend
	같은 목적의 양식을 그룹화<fieldset> 하여 제목<legend>을 지정
	disabled
	form
	name


 select datalist optagroup option
	옵션<option>, <optgroup>의 선택 메뉴<select>나 자동완성<datalist>을 제공

 select
	옵션을 선택하는 메뉴
	<select> <option> </option> </select> 

 optgroup
	option을 그룹화
	label로 분리시켜 제목을 적을 수 있다.

 option
	선택 메뉴<select> '선택 되어 있는 상태' 나 자동완성<datalist>'option에 있는 datalist를 ' input에서 자동 완성되어 사용 가능.

 progress
	작업의 완료 진행률을 표시
	max - 작업의 총량
	value - 작업의 진행량


전역속성
	모든 html 요소에서 공통적으로 사용 가능한 속성

 class
	공백으로 구분된 요소의 별칭을 지정
	css혹은 javascript의 요소 선택기를 통해서 요소를 선택하거나 접근

 id
	문서에서 고유한 식별자를 정의
	css혹은 javascript의 요소 선택기를 통해서 요소를 선택하거나 접근

 style
	요소에 적용할 css를 적용

 title
	요소의 정보(설명)을 지침

  lang
	요소의 언어를 지정

 data-* ex. data-my-age
	사용자가 정의 데이터 속성을 지정
	html에 javascript에서 이용할 수 있는 데이터(정보)를 저장하는 용도로 사용

 draggable
	요소가 Drag and drop api를 사용 가능한지 여부를 지정

 hidden
	요소를 숨김

 tabindex
	tab키를 이용해 요소를 순차적으로 포커스 탐색할 순서를 지정.
	대화형 콘텐츠(interactive content)는 기본적으로 코드 순서대로 탭 순서가 지정됨.

	비대화형 콘텐츠에 tabindex="0"을 지정하여 대화형 콘텐츠와 같이 탭 순서를 사용.

	tabindex="-1"을 통해 포커스는 가능하지만 탭 순서에서 제외 가능
	tabindex="1" 이상의 양수 값은 논리적 흐름을 방해하기 때문에 추천하지 않음.

 상대경로
	선택한 파일 기준으로 경로를 찾는다.
	./
	../

 절대경로
	전체적인 경로를 나타낸다.
	http
	/

주석
 <!--  -->

특수 기호
& n b s p;
& l t; 
& g t;

emmet 문법
	.box 는 div class box를 create
	ul.list는 ul class list를 create
	.container>ul.list>li.list-item*10>a{list$}


	css에서는 h:100 w:100