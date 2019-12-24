<template>
  <g-link v-if="theme === 'dark'" to="/"><g-image src="../../static/logo_dark_mode.svg" class="w-40" alt="logo" /></g-link>
  <g-link v-else to="/"><g-image src="../../static/logo.svg" class="w-40" alt="logo" /></g-link>
</template>

<static-query>
query {
  metadata {
  siteName
  }
}
</static-query>

<script>
export default {
  data() {
    return {
      darkTheme: false
    }
  },
  mounted() {
    this.theme = localStorage.getItem('theme') || 'dark'
    if (window.__theme == 'dark') this.darkTheme = true
  }
}
</script>

<style lang="scss">

</style>