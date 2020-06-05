<template>
  <nuxt-content :document="document" />
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const document = await $content('equations').fetch()

    return {
      document
    }
  }
}
</script>
