<template>
  <w-app id="app">
    <Header /> 
    
    <MainBody />
  
    <footer class="text-center footer">Copyright 2021, Adam Nowland</footer>
  </w-app>
</template>

<script>
  import Header from './components/Header.vue'
  import MainBody from './components/MainBody.vue'


  export default {
    name: 'App',
    data(){
      return {
        posts: []
      }
    },
    components: {
      Header,
      MainBody
      
    },
    methods: {
      async getPost(){
        const res = await fetch('http://localhost:5000/api/posts')
        const data = await res.json()
        console.log(data)
        return data
      }
    },
    created(){
      this.posts = this.getPost()
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 50px;
}
.footer{
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
}
</style>
