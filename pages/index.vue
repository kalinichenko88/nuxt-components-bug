<template>
  <NuxtContent :document="page" />
</template>

<script>
export default {
  async asyncData(ctx) {
    const page = await ctx.$content('hello').fetch()

    return {
      page
    }
  },
  data() {
    return {
      page: undefined
    }
  }
}
</script>
