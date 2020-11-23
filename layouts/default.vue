<template>
  <v-app>
    <Header />

    <v-main>
      <nuxt />
    </v-main>

    <Footer/>
  </v-app>
</template>
<script>
  import Header from '~/components/Sections/Header'
  import Footer from '~/components/Sections/Footer'

  export default {
    components: {
      Header,
      Footer
    }
  }
</script>
<style lang="scss">
</style>
