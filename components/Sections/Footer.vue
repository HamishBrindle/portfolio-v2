<template>
  <v-footer color="transparent" flat app>
    Footer
  </v-footer>
</template>
<script>
export default {
  computed: {
    year () {
      return new Date().getFullYear()
    }
  }
}
</script>

<style lang="scss">

</style>

