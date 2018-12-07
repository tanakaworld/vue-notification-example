<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        vue-notification-example
      </h1>
      <h2 class="subtitle">
        My majestic Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a>
      </div>
      <div class="links">
        <button
          class="button--green"
          @click="show">Show</button>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  methods: {
    show() {
      console.log('show')
      this.$notify({
        group: 'test1',
        title: 'Important message',
        text: 'Hello user! This is a notification!'
      })
    }
  }
}
</script>
