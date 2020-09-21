# HTML

<details>
<summary>목차</summary>

* [HTML5 기초](#HTML5-기초)
    * [HTML 기본 용어](#HTML-기본-용어)
    * [HTML5 페이지 구조](#HTML5-페이지-구조)
* [기본 태그](#기본-태그)
    * [글자 관련 태그](#글자-관련-태그)
    * [목록 관련 태그](#목록-관련-태그)
    * [표 관련 태그](#표-관련-태그)
    * [공간 분할 태그](#공간-분할-태그)
* [HTML 관련 VScode Extensions](#HTML-관련-VScode-Extensions)
* [멀티미디어 관련 태그](#멀티미디어-관련-태그)
    * [이미지 태그](#이미지-태그)
    * [오디오 태그](#오디오-태그)
    * [비디오 태그](#비디오-태그)
* [입력 양식 태그](#입력-양식-태그)
    * [form 태그](#form-태그)
    * [input 태그](#input-태그)
    * [textarea, select, button 태그](#textarea,-select,-button-태그)
    * [fieldset과 legend 태그](#fieldset과-legend-태그)

</details>

## HTML5 기초

### HTML 기본 용어

**태그<sup>tag</sup>**

- HTML 페이지에서 객체를 만들 때 사용
- 일반적으로 시작 태그와 끝 태그가 쌍을 이룸
- 단독으로 사용하는 태그도 존재(끝 태그 X)
- 일부 태그는 태그 내부에 다른 태그가 포함될 수 있음
- 사용 가능한 표준 태그는 W3C 재단에서 결정

![](./images/tag.jpg)

**요소<sup>element</sup>**
- 태그를 사용해 만들어진 객체

![](./images/element.jpg)

**속성<sup>attribute</sup>**
- 태그에 정보를 추가할 때 사용
- 태그마다 가질 수 있는 속성도 W3C 재단에서 표준으로 정의

![](./images/attribute.jpg)

**주석<sup>comment</sup>**
- HTML 코드를 설명하기 위해 작성
- <!-<!---->- 와 --> 사이에 작성

```html
<!-- 이것은 주석입니다. -->
```

<br>

### HTML5 페이지 구조

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>HTML5 Page</title>
</head>
<body>
  <h1>HTML5 Page</h1>
</body>
</html>
```
**!doctype**
- HTML의 버전을 명시
- HTML5는 !doctype 다음에 html이라고 작성
- [다른 버전 설명](#https://en.wikipedia.org/wiki/Document_type_declaration)

**html 태그**
- 모든 HTML 페이지의 루트root 요소
- 모든 HTML 태그는 html 태그 내부에 작성
- lang 속성에는 사용하는 언어를 설정

**head 태그**
- HTML 페이지의 여러 정보들을 제공
- head 태그에는 다음과 같은 태그만 포함 가능

|태그이름|설명|
|-|-|
|meta|웹 페이지에 추가 정보 전달|
|title|웹 페이지의 제목|
|script|웹 페이지에 스크립트 추가|
|link|웹 페이지에 다른 파일 추가|
|style|웹 페이지에 스타일시트 코드 추가|
|base|웹 페이지의 기본 경로 지정|
|||

**body 태그**
- 실제 사용자에게 보여지는 내용을 작성하는 부분

<br>

## 기본 태그

### 글자 관련 태그

**제목<sup>header</sup> 태그**
- 제목을 나타내기 위한 태그
- h1 ~ h6

**본문 관련 태그**
|태그이름|설명|
|-|-|
|p|단락<sup>paragraph</sup>를 나타내는 태그|
|br|줄바꿈 태그|
|hr|수평줄을 긋는 태그|
|||

**글자 형태 관련 태그**
|태그이름|설명|
|-|-|
|b|굵은 글자|
|i|기울어진 글자|
|small|작은 글자|
|sub|아래첨자|
|sup|윗첨자|
|ins|밑줄 글자|
|del|취소선이 그어진 글자|
|||

**앵커<sup>anchor</sup> 태그**
- 페이지 내에 다른 위치로 이동할 때 사용
- 또는 다른 웹페이지로 이동할 때 사용
- Hyper Text
- a 태그를 사용
- a 태그의 href 속성값으로 이동하고자 하는 요소의 위치 또는 문서의 위치 설정

<br>

### 목록 관련 태그

|태그이름|설명|
|-|-|
|ul|순서가 없는 목록을 만드는 태그|
|ol|순서가 있는 목록을 만드는 태그|
|li|ul 또는 ol 태그 내부에서 사용하며 목록의 아이템들을 나타내는 태그|
|||

<br>

### 표 관련 태그

**table 태그**
- 표를 만들기 위한 태그
- 다른 태그보다 사용이 다소 복잡하며, 아래의 태그들이 table 태그 안에서 사용

|태그이름|설명|
|-|-|
|caption|표의 제목<sup>caption</sup>을 작성하기 위한 태그|
|thead|표의 헤더를 만들기 위한 태그|
|tbody|표의 몸체를 만들기 위한 태그|
|tfoot|표의 푸터<sup>footer</sup>를 만들기 위한 태그|
|tr|표의 행을 생성하는 태그|
|th|표의 제목 셀cell을 생성하는 태그<br>tr 태그 내부에서 사용|
|td|표의 데이터 셀<sup>cell</sup>을 생성하는 태그<br>tr 태그 내부에서 사용|
|||

**th,td 태그의 속성**
**rowspan**
- 사용하는 행의 크기를 지장하는 속성(행 병합 효과)
- 예) rowspan="2"는 해당 셀이 행을 2칸 쓰겠다는 의미

**colspan**
- 사용하는 열의 크기를 지정(열 병합 효과)
- 예) colspan="2"는 열을 2칸 쓰겠다는 의미

<br>

### 공간 분할 태그

**inline 요소와 block 요소**
- inline 요소: 옆으로 나열되는 요소(a 태그, 글자 형태 관련 태그 등)
- block 요소: 위에서 아래로 쌓이는 형태로 나열되는 요소(제목 태그, p 태그 등)

**div 태그**
- block 형식의 공간을 생성하는 태그

**span 태그**
- inline 형식의 공간을 만드는 태그

**시맨틱<sup>semantic</sup> 구조 태그**
- HTML5에 추가된 태그
- 페이지의 구조를 의미적으로 분석이 가능
- div와 같은 비슷한 역할이지만 태그에 의미가 있다는 것이 차이

|태그이름|설명|
|-|-|
|header|페이지의 헤더 영역|
|nav|내비게이션 영역|
|aside|사이드에 위치하는 공간|
|section|여러 중심 내용(article 등)을 감싸는 공간|
|footer|페이지의 푸터 영역|
|||

## HTML 관련 VScode Extensions

|이름|설명|
|-|-|
|Auto Rename Tag|태그를 수정할 때 시작 태그와 닫기 태그를 같이 수정해야 하는 번거로움을 해소|
|htmltagwrap|선택 영역을 태그로 감싸야 하는 경우 유용한 확장 기능|
|||

## 멀티미디어 관련 태그

### 이미지 태그

### 오디오 태그

### 비디오 태그

## 입력 양식 태그

### form 태그

### input 태그

### textarea, select, button 태그

### fieldset과 legend 태그