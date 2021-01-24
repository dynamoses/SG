<template>
  <div class="story">
    <pre>{{ story }}</pre>
  </div>
</template>

<script>
export default {
  props: {
    story: { type: Object, required: true }
  }
}
</script>

<style lang="scss">
/* Component specific styles can go here */
.story {
  pre {
    font-weight: bold;
  }
}
</style>
