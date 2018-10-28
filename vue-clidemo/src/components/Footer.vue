<template>
  <footer v-on:click="changeTitle2">
      <p>{{copyright}}{{title1}}</p>
  </footer>
</template>

<script>
export default {
  name: 'app-footer',
  props:{
      title1:{
          type:String
      }
  },
  data () {
    return {
        copyright:"vue.js footer"
    }
  },
  methods:{
      changeTitle2:function(){
          this.$emit("changeTitle2","父向子传值");
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer{
    height: 100px;
    width: 100vw;
    padding: 30px;
    background: lightgreen;
    text-align: center;
}
p{
    color: white;
}
</style>
