<template>

  <div class="black-bg" v-if="modalCondition == true">
    <div class="white-bg">
        <h4>상세페이지</h4>
        <p>상세페이지 내용</p>
        <button @click="modalCondition=false">닫기</button>
    </div>
  </div>



  <div class="Menu">
    <a v-for="(menu,id) in menus" :key="id"> {{ menu }}</a>
    <!--
      <a>Home</a>
      <a>Shops/a>
      <a>About</a>
     -->
  </div>
   <div>
     <img src="./assets/room0.jpg" class="room-img">
    <h4 @click="modalCondition=true">{{ products[0] }}</h4>
    <p>60 만원</p>
    <button @click="reportCount[0]++">허위매물신고</button> 
    <span>신고 수 : {{ reportCount[0] }}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{ products[1] }}</h4>
    <p>70  만원</p>
    <button @click="reportCount[1]++">허위매물신고</button> 
    <span>신고 수 : {{ reportCount[1] }}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" class="room-img">
    <h4>{{ products[2] }}</h4>
    <p>100 만원</p>
    <button @click="reportCount[2]++">허위매물신고</button> 
    <span>신고 수 : {{ reportCount[2] }}</span>
  </div>
</template> 

<script>

export default {
  name: "App",
  data(){
    return {
      modalCondition : false,
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      menus : ['Home', 'Shops', 'About'],
      reportCount : [0,0,0],
    } 
  },
  components: {
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
/* 모달창 디자인 */
body {
  margin:0
}

div {
  box-sizing:border-box;
}

.black-bg {
  width:100%;
  height:100%;
  background:rgba(0,0,0,0.5);
  position:fixed;
  padding:20px;
}

.white-bg {
  width:100%;
  background:white;
  border-radius:8px;
  padding:20px;
}
/* 메뉴탭 스타일 */
.Menu {
  background: darkslateblue;
  padding:15px;
  border-radius:5px;
}

.Menu a {
  color:white;
  padding:10px;
}

.room-img {
  width:100%;
  margin-top:40px;
}
</style>
