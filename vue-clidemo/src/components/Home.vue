<!-- 模板：html结构 -->
<template>
  <div id="home">
    <app-header v-bind:title1="title1"></app-header>
    <users v-bind:users="users"></users>
    <app-footer v-on:changeTitle2="titlechanged($event)" v-bind:title1="title1"></app-footer>
  </div>
</template>

<!-- 行为：处理逻辑 -->
<script>

import users from './users'
import Header from './Header'
import Footer from './Footer'

export default {
  name: 'home',
  data(){
    return {
      // tittle:"这是我的第一个脚手架项目！"
      users:[
        {name:"Henry",position:"web开发",show:false},
        {name:"Henry",position:"web开发",show:false},
        {name:"Henry",position:"web开发",show:false},
        {name:"Henry",position:"web开发",show:false},
        {name:"Henry",position:"web开发",show:false},
        {name:"Henry",position:"web开发",show:false},
        {name:"Henry",position:"web开发",show:false}
        ],
        title1:"传值改变的是单个项目"
    }
  },
  methods:{
    titlechanged:function(tl){
      this.title1 = tl;
    }
  },
  components: {
    "users":users,
    "app-header":Header,
    "app-footer":Footer
  },
  created(){
      this.$http.get("http://jsonplaceholder.typicode.com/users").then((data)=>{
        //   console.log(data);
        this.users = data.body;
      })
  }
}
</script>

<!-- 样式：解决样式-->
<style>
h1{
  color:purple;
}
</style>
