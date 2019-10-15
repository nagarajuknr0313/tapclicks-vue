<template>
  <div id="app">
<<<<<<< HEAD
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
=======
    <div class="columns" style="margin-top: 3px;">
<div class="column is-one-fifth" >
     <sidebar> </sidebar>
>>>>>>> 3e553be8e4f7e75e970218be80fb592e91ff07bb
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
  background-color: #42b983;
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