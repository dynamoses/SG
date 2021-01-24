<template>
  <div>
    <header class="header">
      <img class="header__image" src="../assets/img/sungod-black.png">
    </header>
    <h1 class="page-title">
      Stories
    </h1>
    <div class="stories">
      <Story v-for="story in stories" :key="story.id" :story="story" />
      <Story v-for="story in stories" :key="story.id" :story="story" />
      <Story v-for="story in stories" :key="story.id" :story="story" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    stories: { type: Array, required: true }
  }
}
</script>

<style lang="scss">
/* Component specific styles can go here */
</style>
