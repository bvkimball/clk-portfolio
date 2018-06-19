<template>
  <section class="container">
    <app-logo/>
    <app-sub-logo/>
    <app-menu/>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import AppSubLogo from '~/components/AppSubLogo.vue'
import AppMenu from '~/components/AppMenu.vue'

export default {
  components: {
    AppLogo,
    AppSubLogo,
    AppMenu
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Merriweather:400,700');
@import "~/assets/less/app.less";

.container {
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
