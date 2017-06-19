import Vue from 'vue' 
<template>
  <div class="hello">
    <h1>{{msg}}</h1>
    <span>{{msg}}</span>
    <span v-text="msg"></span>
    <span v-html="msg"></span>
    <p>{{$route.params.color}}</p>
    <button @click="getParam">get param</button>
     <router-view></router-view>
  </div>
</template>

<script>
export default {
   name:'hello',
   data(){
       return{
           msg:'<p>i am an apple</p>'
       }
   },
   methods:{
       getParam(){
           console.log(this.$route.params)//注入参数
       }
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>