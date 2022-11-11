<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <div :style="{fontSize:postFontSize+'em'}" >
  <BlogPost v-for="post in posts" :key="post.id" :title="post.title" @enlarge-text="postFontSize+=1"></BlogPost>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import BlogPost from './components/BlogPost.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    BlogPost
},
  data(){
    return{
      posts:[
        {id:1,title:'My journey with Vue'},
        {id:2,title:'Blogging with Vue'},
        {id:3,title:'Why Vue is so fun'}
      ],
      postFontSize:1
    }
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
