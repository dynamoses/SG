<template>
  <div class="container">
    <div>
      <template v-if="loaded">
        <p v-if="failure">
          Unable to load stories from API, if this persists please create dummy data to complete the task.
        </p>

        <Stories v-else :stories="stories" />
      </template>

      <p v-else>
        Loading...
      </p>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $axios }) {
    try {
      const { results } = await $axios.$get('stories/', { params: { limit: 3 } })
      return { loaded: true, failure: false, stories: results }
    } catch (error) {
      // eslint-disable-next-line no-console
      console.log(error)
      return { loaded: true, failure: true }
    }
  }
}
</script>
