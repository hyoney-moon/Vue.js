<template>
<!-- 모달창 -->
<div class="black-bg" v-if="openModal ==  true">
  <div class="white-bg">
    <h4 >상세페이지임</h4>
    <p>상세페이지 내용임</p>
    <img @click="openModal = false" src="./assets/exit.png" class="exit-img">
  </div>
</div>

  <!-- 반복문 -->
  <div class="menu">
<!-- <a>Home</a>
    <a>Products</a>
    <a>About</a> -->
    <!-- :key="작명" 반복문에서 안쓰면 에러남 
    횟수 부분에 데이터를 넣을 수 있음, 데이터 저장 후 사용-->
    <a v-for="a in menus" :key="a">{{ a }}</a>
  </div>
    <!-- 애초에 바뀔일이 없으면 안해도 됨
    HTML 속성도 데이터바인딩 가능 속성 앞에 : 붙임, {{이거 아님}} 👉 :속성="데이터이름"
    <h4 class="red" :style="style1"> {{products[0]}} 원룸</h4>
    script에 선언한 {{ 데이터이름 }}
    자주 변할거같은 데이터들은 데이터로 보관하고 HTML에 {{데이터바인딩}} -->
  <!-- <div v-for="(a,i) in products" :key="i">  
    <h4>{{ a }} 원룸</h4>
    <p>{{ price1 }} 만원</p>
  </div> -->
  <div>
    <img :src="rooms[0].image" class="room-img">
    <h4 @click="openModal = true">{{rooms[0].title}}</h4>
    <p>{{rooms[0].price}} 원</p>
    <button @click="report[0]++">허위매물신고</button>
    <span> 신고수 : {{ report[0] }}</span>
  </div>
  <!-- v-for 사용 -->
  <div v-for="(a,i) in rooms" :key="i">
    <img :src="a.image" class="room-img">
    <h4>{{a.title}}</h4>
    <p>{{a.price}} 원</p>
  </div>
</template>

<script>

// import roomInfo from './assets/roomInfo.js';
// roomInfo;

// import 여러개일 때
// import {변수명1, 변수명2} from '경로';
// 변수명1

import roomInfo from './assets/roomInfo.js';

export default {
  name: 'App',
  data(){
    return{
      rooms : roomInfo,
      openModal : false,
      report : [0,0,0],
      price1 : 60,
      price2 : 70,
      style1 : 'color : blue',
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      menus : ['Home', 'Shop', 'About'],
    }
  },
  methods : {
    // function 넣는 곳
    increase(){
      // function 안에 데이터 쓸 때 this.데이터명
      this.report += 1;
    }
  },
  components: {

  }
}
</script>

<style>
body {
  margin: 0;
}
/* 모달창 디자인 */
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
.room-img {
  width: 100%;
  margin-top: 40px;
}
.exit-img {
  width: 20px;
}
</style>
