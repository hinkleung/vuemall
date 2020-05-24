<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import axios from 'axios'
import jsonp from 'jsonp'

export default {
  name: 'App',
  components: {
    HelloWorld
  },

  data(){
    return {
      age:30,
      data:''
    }
  },

  mounted(){
    //CROS跨域解决(后端改)
    // let url = 'https://www.easy-mock.com/mock/5b012c1fe6e1035843cd3aff/mockapi/table/list'
    // axios.get(url).then(()=>{
      
    // })

    //JSONP跨域解决(前端加插件、后端小改)
    // let url2 = '/search/hotwords'
    // jsonp(url2,(err,res)=>{
    //   let result = res;
    //   this.data = result;
    // })

    //接口代理
    let url2 = '/api/search/hotwords'
    jsonp(url2,(err,res)=>{
      let result = res;
      this.data = result;
    })
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
