<template>
  <h1>Post Lists</h1>
  <div v-for="post in posts" :key="post.id">
    <SinglePost :post="post"></SinglePost>
  </div>
</template>

<script>
import { onMounted, onUnmounted, onUpdated } from 'vue'
import SinglePost from './SinglePost'
export default {
  components: { SinglePost },
props:['posts'],
    setup(props){
        onMounted(()=>console.log("mounted"));
        onUnmounted(()=>console.log("unmunted"));
        onUpdated(()=>console.log("updated"))
    }
}
</script>
<style>

</style>