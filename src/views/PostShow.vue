<template>
  <div class="post">
    <h1>This is an Post Show page</h1>
    <div>{{ post.id }}</div>
    <div>{{ post.title }}</div>
    
  </div>
  
</template>
<script>
export default {
  props:{
    id:{
      type:String,
      required:true,
    }
  },
  data(){
    return {
      posts: [
        {
          id:1,
          title:'vue.js'
        },
        {
          id:2,
          title:'react'
        },
        {
          id:3,
          title:'alpine.js'
        }
      ]
    }
  },
  computed:{
    post(){
      return this.posts.find(post => post.id == this.id)
    }
  },
  mounted(){
    console.log(this.$route)
  }
}
</script>