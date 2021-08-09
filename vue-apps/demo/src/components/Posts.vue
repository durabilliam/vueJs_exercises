<template>
  <div class="container">
    <table class="table table-striped mt-4">
      <thead>
        <tr>
          <th scope="col">UserId</th>
          <th scope="col">Id</th>
          <th scope="col">Title</th>
          <th scope="col">Body</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="post in posts" :key="post.id">
          <td>{{ post.userId}}</td>
          <td>{{ post.id }}</td>
          <td>{{ post.title }}</td>
          <td>{{ post.body }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>

import axios from 'axios';

export default {
  name: "PostsExample",
  data() {
    return {
      posts: [],
      // posts: [
      //   { id: 1, title: 'Post 1', body: 'jiarfshviua'},
      //   { id: 2, title: 'Post 2', body: 'jekrwhvei5u'},
      //   { id: 3, title: 'Post 3', body: 'jfhiuhtucho'},
      //   { id: 4, title: 'Post 4', body: 'kwjerconut9'},
      // ],
    };
  },

  created(){
    axios.get('https://jsonplaceholder.typicode.com/posts').then(posts => {
      this.posts = posts.data
    }) ;
  }
};
</script>

<style>
</style>
