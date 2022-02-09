### Vue.js Theory 02
----
#### 기본적인 문법
```
<template>
    <div>
        <h1>template 안에 기본적인 css/HTML처럼 입력해주면 됨</h1>
    </div>
</template>
```
```
<script>
//기능 개발 관련 vue 문법 적용 시키기
export default {
    name : 'App',
    data(){
        return{}
    },
    component: {
        //object 자료형으로 저장
        //{자료이름 : 자료내용}
    }
}
</script>
```
```
<!-- HTML 속성도 데이터바인딩 가능 속성 앞에 : 붙임, {{이거 아님}} 👉 :속성="데이터이름" -->
    <h4 class="red" :style="style1"> XX 원룸</h4>
```
#### {{데이터 바인딩}} 용도
1. HTML에 하드코딩 해놓으면 나중에 변경 어려움
2. Vue의 실시간 자동 렌더링
    + Vue는 data를 변경하면 data와 관련된 HTML에도 실시간으로 반영됨
    + 그래서 {{데이터바인딩}} 써야함
    + 실시간 바인딩 사용하면 웹앱 만들기 좋음
3. 자주 안 바뀔 것 같은면 {{데이터바인딩}} 안해도 됨

#### 반복문
```
<!-- 반복문에서 :key="" 안쓰면 에러남 -->
<태그 v-for="작명 in 몇회" :key="작명"></a>
<a v-for="i in menus" :key="i"> {{ i }} </a>
```
Script에 데이터 저장 후 몇회 부분에 넣을 수 있음
#### ⭐ :key="작명" 의 용도 ⭐
- 반복문 쓸 때 꼭 써야함
- 반복문이 사용될 태그를 구분하기 위한 용도
- 변수명 2개까지 가능

#### Event Handler
- onClick : `v-on:click="Js"` or `@click="Js"`
- mouseover : `@mouseover="js"`
✴ 입력할 코드가 길 때 👉 함수 만들어서 사용
- function : data 뒤에 `methods : { function(){} }`

#### Img
assets : 상대 경로로 집어넣을 이미지나 이런거 넣어 놓는 곳

#### 모달창
[모달창 디자인] 👉 [style] 👉 
```
동적인 UI 만드는 법
1. UI의 현재 상태를 데이터로 저장해 둠
    - 그 UI가 지금 어떻게 보여야함? true/false
2. 데이터에 따라 UI가 어떻게 보일지 작성
    - v-if="조건문" (조건문이 true일 때만 작동)
```
#### import/export
다른 파일 vue에 import
`export default 변수명` `import 변수명 from 파일경로`