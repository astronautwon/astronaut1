### 학습목표
- CSS를 왜 사용하는지 설명할 수 있다.
- CSS의 기본 문법과 구조를 설명할 수 있다.
- HTML에 CSS를 적용하는 방법에 대해 이해할 수 있다.
 
# CSS

![html-css](https://user-images.githubusercontent.com/104332696/167093819-d719eef2-a551-4ab3-ae1a-3b8c2fed30e0.jpg)

- 구조 : 웹 콘텐츠에 의미를 부여하고 구조를 형성 → HTML
- 표현 : 시각적인 디자인과 레이아웃 표현 → CSS
- CSS는 Cascading Style Sheet의 약어
- CSS는 HTML로 부터 디자인적인 요소를 분리해 정의할 수 있음.

### CSS의 기본구조

CSS는 선택자와 선언부로 구성된다. 선택자는 스타일을 지정할 HTML 요소(태그,아이디 등)를 가리킨다. 선언부에는 CSS 속성 이름과 값이 포함된다. 속성이 여러 개일 경우, 한 줄로 나열해도 상관없지만 여러 줄에 걸쳐 작성하는 것이 좋다.

```css
선택자  {속성:값; 속성:값....}

예)
/* h1태그의 색상을 빨간색으로 크기는 15px로 지정합니다.*/
h1 {color:red; font-size:15px;}
```

- CSS 구문은 선택자(selector)와 선언부(declaration)로 구성.
- 선택자는 디자인을 적용하고자 하는 HTML요소. -> 선택자 정의가 중요
- 선언부는 콜론(:)으로 구분 되어진 다수의 항목을 포함.
- 각 선언은 항상 세미콜론(;)으로 끝나며, 선언블록은 중괄호({ })로 묶음.
- /* comment */은 코드를 설명하는 데 사용됨.

`선택자의 중요성`

CSS의 핵심은 적절한 선택자를 사용하는 것이며 복잡한 문서 구조에서 특정 부분을 선택하기 위한 선택자 지정은 어려울 수 있으며 html 구조를 처음부터 잘 설계하는 것이 중요함.

### CSS 적용 방법

HTML 문서에 CSS를 적용하는 방법에는 내부 스타일시트, 외부 스타일시트, 인라인 스타일 등 총 3가지 방법이 있다

![css2](https://user-images.githubusercontent.com/104332696/167096146-6a69d9a4-5e8c-436f-9281-551291d3d248.jpg)


1. 내부 스타일 시트
html 파일에 스타일을 기술하는 방법으로 <head></head> 태그 사이에 <style></style> 태그 부분에 작성함. 
html 과 css 가 한 파일에 있으므로 작업이 쉽고 간편하지만 css의 재활용이 안되는 문제가 있어 특별한 경우가 아니면 외부 스타일시트가 권장 됨

```css
<head>
<style>
body {
    background-color: red;
}

h1 {
    color: maroon;
    margin-left: 40px;
} 
</style>
</head>
<body>
    ...
</body>
```


2. 외부 스타일 시트

css 를 작성하는 가장 기본적인 방법 별도의 파일에 CSS 문서를 작성하고 해당 CSS를 필요로 하는 html 문서에서 불러와 사용하는 형식이다 
이때 css는 동일한 서버에 있어도 되고 url을 통해 다른 서버의 css를 불러오는 것도 가능하다

```css
link rel="stylesheet" type="text/css" href="mystyle.css">
<link rel="stylesheet" type="text/css" href="http://cdn.site.com/css/mystyle.css">
```

3.인라인 스타일

html 태그에 필요한 디자인 속성을 직접 작성하는 형식이다. 그때 그때 필요한 디자인을 바로 적용할 수 있다는 편리함이 있지만 일관된 디자인 체계를 유지하는 데에는 방해가 되기 때문에 꼭 필요한 경우가 아니라면 사용하지 않도록 한다.

```css
<h1 style="color:blue; margin-left:30px;">This is a heading</h1>
```

### <우선 순위>

브라우저 디자인 정의 -> 외부 스타일시트 -> 내부 스타일시트 -> 인라인 스타일시트

낮은순 -> 높은 순
