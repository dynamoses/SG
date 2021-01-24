<template>
  <div class="stories">
    <Story v-for="story in stories" :key="story.id" :story="story" />
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
