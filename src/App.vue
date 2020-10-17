<template>
  <div id="app">
    <Welcome />
    <Book :bookjson="bookjson" />
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
import book from "@/content/book.json"
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
      bookjson: book,
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