<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    <div class="columns" style="margin-top: 3px;">
<div class="column is-2" >
     <sidebar> </sidebar>
    </div>
     <div class="column is-9 ">
             <div class="container" >
    <section class="slider-panel bottom">
      <span class="headstyle">
        <span style="color:blue"><b-icon custom-size="mdi-18px"
                      pack="fas"
                      icon="arrow-left"
                      size="is-small"
                      >
                  </b-icon></span>&nbsp;
               <span style="font-size: 20px;">Order name</span>     </span>
      <b-tabs :animated="false">
        <b-tab-item label="info">
          <b-collapse class="" aria-id="contentIdForA11y3">
            <div
                slot="trigger" 
                slot-scope="props"
                class="card-header"
                role="button"
                aria-controls="contentIdForA11y3">
                 <a class="header-icon">
                    <b-icon
                        :icon="props.open ? 'chevron-down' : 'chevron-up'">
                    </b-icon>
                </a>
                <p class="header-title">
                    Component
                </p>
               
            </div>
            <div class="content">
                <div class="content">
                   <div>
                    
                      <b-field label="Name">
            <b-input value="Kevin Garvey"></b-input>
        </b-field>
                   </div>
                </div>
            </div>
        </b-collapse>
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
.headstyle{
      padding-right: 87%;
}
</style>