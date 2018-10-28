<template>
  <div class="use">
     
      <ul>
          <li v-for="user in users" v-on:click="user.show = !user.show">
              <h1> {{user.name}}</h1>
              <h1 v-show="user.show"> {{user.position}}</h1>
          </li>
      </ul>
      <button v-on:click="deleteObject">删除</button>
  </div>
</template>
<!-- 传值：string number boolean
     引用:array object
 -->
<script>
export default {
  name: 'users',
//   props:["users"],
    props:{
        users:{
            type:Array,
            required:true
        }
    },
    data () {
        return {
        
        }
    },
    methods:{
        deleteObject:function(){
            this.users.pop();
        }
    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.users{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
}

ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}

li{
    flex-grow: 1;
    flex-basis: 200px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
}
</style>
