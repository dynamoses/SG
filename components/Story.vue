<template>
  <div class="story">
    <div class="story__image-container">
      <img class="story__image" :src="story.cover_img" :alt="story.title">
    </div>
    <div class="story__text-container">
      <div class="blog-header">
        <div>
          <span class="category">{{ story.category }}</span>
        </div>
        <div class="date-posted">
          {{ datePosted }}
        </div>
      </div>
      <h1 class="h1">
        {{ story.title }}
      </h1>
      <div class="subtitle">
        {{ story.desc }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    story: { type: Object, required: true }
  },
  computed: {
    datePosted () {
      const dateArray = this.story.date.split('-').reverse().join('/')
      return dateArray
    }
  }
}
</script>

<style lang="scss">
@import '../scss/_variables.scss';
@import '../scss/main.scss';
</style>
