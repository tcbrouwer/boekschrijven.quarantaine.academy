<template>
  <b-card
    style="min-width: 15rem; max-width: 25rem;"
    class="m-3"
  >
    <b-list-group flush>
        <b-list-group-item v-for="(paragraph, index) in paragraphs" :key="index">
            {{ paragraph }}
        </b-list-group-item>
    </b-list-group>
  </b-card>
</template>

<script lang="ts">
export default {
  name: "Chapter",
  props: ["chapter"],
  computed: {
    paragraphs() {
      return this.chapter
    },   
  },
};
</script>

<style scoped>
</style>