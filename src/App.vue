<template>
  <div id="app">
    <div class="columns" style="margin-top: 3px;">
<div class="column is-2" >
     <sidebar> </sidebar>
    </div>
     <div class="column is-9 ">
             <div class="container" >
    <section class="slider-panel bottom">
      <span class="headstyle">
              <b-icon custom-size="mdi-18px"
                      pack="fas"
                      icon="user"
                      size="is-small">
                  </b-icon> <span style="font-size: 20px;">Order name</span>     </span>
      <b-tabs :animated="false">
        <b-tab-item label="info">
        </b-tab-item>
        <b-tab-item label="line items">
        </b-tab-item>
      </b-tabs>
    </section>
   
  </div>
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
.headstyle{
      padding-right: 87%;
}
</style>