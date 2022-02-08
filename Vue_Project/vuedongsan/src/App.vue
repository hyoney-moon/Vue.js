<template>

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
  <div v-for="(a,i) in products" :key="i">  
    <h4>{{ a }} 원룸</h4>
    <p>{{ price1 }} 만원</p>
  </div>
  <!-- <div>
    <h4>{{products[1]}} 원룸</h4>
    <p>{{ price2 }} 만원</p>
  </div>
  <div>
    <h4>{{products[2]}} 원룸</h4>
    <p>{{ price2 }} 만원</p>
  </div> -->
</template>

<script>
var array = [10,20,30];
array[0]

export default {
  name: 'App',
  data(){
    return{
      price1 : 60,
      price2 : 70,
      style1 : 'color : blue',
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      menus : ['Home', 'Shop', 'About'],
    }
  },
  components: {

  }
}
</script>

<style>
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
</style>
