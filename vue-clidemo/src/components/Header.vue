<template>
  <header v-on:click="changeTitle">
      <h1>{{tittle}}{{title1}}</h1>
  </header>
</template>

<script>
export default {
  name: 'app-header',
  props:{
      title1:{
          type:String
      }
  },
  data () {
    return {
        tittle:"vue.js"
    }
  },
  methods:{
      changeTitle:function(){
          this.title1 = "change the title";
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
    height: 100px;
    width: 100vw;
    padding: 30px;
    background: green;
    text-align: center;
}
h1{
    color: white;
}
</style>
