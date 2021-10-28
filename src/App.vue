<template>
  <div class="Menu">
    <a v-for="(menu,id) in menus" :key="id"> {{ menu }}</a>
    <!--
      <a>Home</a>
      <a>Shops/a>
      <a>About</a>
     -->
  </div>
  <div>
    <h4>{{ products[0] }}</h4>
    <p>60 만원</p>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>70  만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>100 만원</p>
  </div>
</template> 

<script>

export default {
  name: "App",
  data(){
    return {
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      menus : ['Home', 'Shops', 'About'],
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

.Menu {
  background: darkslateblue;
  padding:15px;
  border-radius:5px;
}

.Menu a {
  color:white;
  padding:10px;
}
</style>
