<template>
  <div id="app">
    <Welcome />
    <Book />
    <CourseCard :course="upstream" />
    <router-view />
  </div>
</template>

<script lang="ts">
// code
import Book from "@/views/Book.vue"
import CourseCard from "@/components/CourseCard.vue"
import Welcome from "@/views/Welcome.vue"

// content
import upstream from "@/news/upstream.json"


export default {
  name: 'App',
  components: {
    Book,
    CourseCard,
    Welcome,
  },
  data() {
    return {
      upstream: upstream
    }
  }
}
</script>

<style>
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>