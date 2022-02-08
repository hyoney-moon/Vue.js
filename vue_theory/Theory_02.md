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

