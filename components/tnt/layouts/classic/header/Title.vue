<template lang='pug'>
span.py-24
  NuxtLink(to='/') {{ title }}
</template>

<script>
export default {
  data () {
    return {
      title: this.$nuxt.$options.head.title
    }
  }
}
</script>

<style lang='postcss' scoped>
span {
  @apply block w-min m-auto text-4xl sm:text-6xl md:text-7xl text-base-content font-poster;
}
</style>
