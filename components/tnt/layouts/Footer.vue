<template lang='pug'>
footer
  .social
    ul
      li(v-for='(item, i) in social' :key='i')
        a(:href='item.to' target='_blank')
          TntSimpleIcon(:icon='item.icon')
  .copyright
    | &copy;
    |
    a(href='https://thombruce.com/') Thom Bruce
    |
    | 2021 - {{ new Date().getFullYear() }}
</template>

<script>
export default {
  data () {
    return {
      title: this.$nuxt.$options.head.title,
      social: [
        {
          icon: 'facebook',
          title: 'Facebook',
          to: 'https://facebook.com/thombruce'
        },
        {
          icon: 'twitter',
          title: 'Twitter',
          to: 'https://twitter.com/thombruce'
        },
        {
          icon: 'github',
          title: 'GitHub',
          to: 'https://github.com/thombruce'
        },
      ]
    }
  }
}
</script>

<style lang='postcss' scoped>
footer {
  @apply mt-5 py-5 bg-light-100 dark:bg-dark-700;
  & .social {
    @apply text-3xl;
    & ul {
      @apply flex justify-center;
      & li a {
        @apply block px-4;
      }
    }    
  }
  & .copyright {
    @apply pt-4 text-center text-sm text-gray-400 dark:text-gray-500;
    & a {
      @apply text-gray-600 hover:text-gray-800 dark:text-gray-300 dark:hover:text-gray-400;
    }
  }
}
</style>
