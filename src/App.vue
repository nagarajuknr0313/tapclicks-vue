<template>
  <div id="app">
    <div class="columns" style="margin-top: 3px;">
<div class="column is-one-fifth" >
     <sidebar> </sidebar>
    </div>
     <div class="column is-9 ">
            <router-view></router-view>
        </div>
    </div>
    
  </div>
</template>
<script>
import sidebar from "./Sidebar.vue";
export default {
  components:{
    "sidebar":sidebar
  }
}
</script>
<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>