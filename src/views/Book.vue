<template>
  <div>
    <h1>{{ book.title }}</h1>
    
    <div v-for="chapter in book.chapters" :key="chapter" class="d-flex justify-content-center">
        <Chapter :chapter = chapter />
    </div>  
  </div>
</template>

<script lang="ts">
import Chapter from '@/components/Chapter.vue'

// This is a stub, should load from server


export default {
  name: 'Book',
  props: [ "bookjson" ],
  components: {
    Chapter,
  },
  computed: {
    book() {
      const defaultTitle = "Choose a title"
      if( this.bookjson === undefined || this.bookjson === null ) {
        return { title: defaultTitle, chapters: [] }
      } else {
        return { 
          title: this.bookjson.title ? this.bookjson.title : defaultTitle,
          chapters: this.bookjson.chapters ? this.bookjson.chapters : []
        }
      }
    }
  },

}
</script>

<style scoped>
</style>