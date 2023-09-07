<template>
  <div id="app">
    <div class="menu">
      <a v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
    </div>
    <div v-for="(info, i) in infos" :key="i">
      <h4>{{ info.product }}</h4>
      <p>{{ info.price }} 만원</p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      menus : ['Home', 'Shop', 'About'],
      infos : [
        {product: '역삼동원룸', price: '50'},
        {product: '천호동원룸', price: '60'},
        {product: '마포구원룸', price: '70'},
      ]
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
