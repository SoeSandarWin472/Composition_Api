<template>
  <div class="home">
    <!-- <input type="text" v-model="search">
    {{ search }}
   <div v-for="name in filter" :key="name">
{{ name }}
   </div> -->
   <div v-if="showPost">

   <PostLists :posts="posts"></PostLists>
   </div>
   <button @click="showPost=!showPost">toggle post list</button>
   <button @click="posts.pop()">delete</button>
  </div>
</template>

<script>
import PostLists from '../components/PostLists'
import { computed, ref } from 'vue'



export default {
  components: { PostLists },
  setup(){
    // let search=ref("")
    // let names=ref(["aungaung","kyawkyaw","susu","mgmg"])

    // let filter=computed(()=>{
    //   return names.value.filter(name=>{
    //     return name.includes(search.value)
    //   })
    // })
    // return {names,search,filter}
  let showPost=ref(true)
    let posts=ref([{title:"post title 1",body:"lorem ipsum",id:1},{title:"post title 2",body:"lorem ipsum",id:2}])
    return {posts,showPost}
  }
}
</script>
