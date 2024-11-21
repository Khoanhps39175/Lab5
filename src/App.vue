<!-- <script setup>
import Bai1 from './components/Bai1.vue';
</script>
<template>
  <Bai1></Bai1>
</template> -->

<!-- <script setup>
import Bai2 from './components/Bai2.vue';
</script>
<template>
  <Bai2></Bai2>
</template> -->

<!-- <script setup>
import Bai3 from './components/Bai3.vue';
</script>
<template>
  <Bai3></Bai3>
</template> -->

<template>
  <div id="app">
    <h1>Ứng dụng Blog nhỏ với Vue.js</h1>
    <CreatePost @add-post="addPost"></CreatePost>
    <PostList :posts="posts"></PostList>
  </div>
</template>

<script setup>

import { ref } from 'vue'
import CreatePost from './components/CreatePost.vue'
import PostList from './components/PostList.vue';

const posts = ref([])

function addPost(post) {
  posts.value.push(post)
}
</script>

<style>
#app {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}
</style>
