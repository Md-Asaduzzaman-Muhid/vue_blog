<template>
    <div class="container">
        <h1 class="text-center mt-5">Posts</h1>
        <div v-for="post in posts" :key="post.id" class="post_single border rounded p-3 mb-2">
            <div class="title">
                <h4><a v-bind:href="post.id"> {{ post.title }} </a></h4>
            </div>
            <div class="body">{{ post.body }}</div>
        </div>
    </div>
</template>

<script>
const axios = require('axios');
export default {
  name: 'UserList',
  props: {
    msg: String
  },
  data(){
   //result: null 
    return{
      posts: []
    }
  }, 
  mounted:function() {
    //let self = this;
    axios.get('https://jsonplaceholder.typicode.com/posts/?')
      .then(response => (this.posts = response.data))
      .catch(function (error) {
        // handle error
        console.log(error);
      })
      .finally(function () {
        console.log('Fatch complite');
      })
  }
}
 
</script>