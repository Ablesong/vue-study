<!-- 模板：html结构 -->
<template>
  <div id="app">
    <a href="/">home</a>
    <a href="/helloworld">hello</a>
    <ul>
      <li><router-link to="/">home</router-link></li>
      <li><router-link to="/helloworld">hello</router-link></li>
    </ul>
    <router-view></router-view>
  </div>
</template>

<!-- 行为：处理逻辑 -->
<script>


export default {
  name: 'App',
  data(){
    return {
      // tittle:"这是我的第一个脚手架项目！"
     
    }
  },
  methods:{
  
  }
}
</script>

<!-- 样式：解决样式-->
<style>
h1{
  color:purple;
}
</style>
