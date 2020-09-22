<template>
  <div class="container">
    <Header />
    <main>
      <Hero />
    </main>
    <Footer />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100vh;
}
</style>

<script>
import Header from './components/Header'
import Hero from './components/Hero'
import Footer from '~/common/Footer'

export default {
  components: {
    Header,
    Hero,
    Footer,
  },
}
</script>
