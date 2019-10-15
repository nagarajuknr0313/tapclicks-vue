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
                    Order Details
                </p>
               
            </div>
            <div class="content">
                <div class="content ">
                   <div class="columns is-multiline ">
                    <div class="column is-6 is-labelstyle " v-for="(products, index) in productList" :key="index">
                      <label style="padding-right: 75%;">{{products.name}}</label>
                      <div  style="padding-left:10%">
            <b-input class="textlabels" :value="products.discripthion" readonly ></b-input>

                      </div>
                    </div>
                     
                   </div>
                </div>
            </div>
        </b-collapse>
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
                    Campaign Details
                </p>
               
            </div>
            <div class="content">
                <div class="content ">
                   <div class="columns is-multiline ">
                    <div class="column is-6 is-labelstyle " v-for="(products, index) in CampineList" :key="index">
                      <label style="padding-right: 50%;">{{products.name}}</label>
                      <div  style="padding-left:10%">
            <b-input class="textlabels" :value="products.discripthion" readonly ></b-input>

                      </div>
                    </div>
                     
                   </div>
                </div>
            </div>
        </b-collapse>
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
                    Finance Overview
                </p>
               
            </div>
            <div class="content">
                <div class="content ">
                   <div class="columns is-multiline ">
                    <div class="column is-6 is-labelstyle " v-for="(products, index) in financeList" :key="index">
                      <label style="padding-right: 38%;">{{products.name}}</label>
                      <div  style="padding-left:10%">
            <b-input class="textlabels" :value="products.discripthion" readonly ></b-input>

                      </div>
                    </div>
                     
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
      data(){
return{
productList:[{name:"Client",discripthion:"johndeo"},
{name:"Salesperson",discripthion:"Jasmine Smith"},
{name:"Satrt Date",discripthion:"jul 9,2018 "},
{name:"End Date",discripthion:"jul 9,2019"},
{name:"Orderd Type",discripthion:"regular"},
{name:"Submited By",discripthion:"Jasmine Smith"}],
CampineList:[{name:"Business Catogory",discripthion:"Retail Store"}],
financeList:[{name:"Suggested Display Budget",discripthion:"$1500"},
{name:"Suggested Search Budget",discripthion:"$1500"},
{name:"Email",discripthion:"Johndeo@testcompany.com"}]
}
    },
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
.input{
        color: #d3d7d9 !important;
    border-color: #fafbfb !important;
    width: 60% !important;
}
.is-labelstyle{
  
    color: #d3d7d9;
    font-size: 18px;
}
.headstyle{
      padding-right: 87%;
}
.is-multiline{
  padding-top:3%;
}
</style>
