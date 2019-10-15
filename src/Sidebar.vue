<template>
    <div>
       <template>
    <b-menu class="sidebar">
        <b-menu-list >
            <b-menu-item  active label="Data"></b-menu-item>
            <b-menu-item  label="Products" @click="gotolayout()"> </b-menu-item>
            <b-menu-item  label="Cart"></b-menu-item>
            <b-menu-item  label="login"  tag="router-link"  to="/login"></b-menu-item>
            <b-menu-item icon="information-outline" label="Info"></b-menu-item>
        </b-menu-list>
       
    </b-menu>
    
</template> 
    
    
    </div>
</template>

<script>
export default {
   methods:{
       gotolayout(){
           this.$router.push('/productlist');
       }
   } 
}
</script>