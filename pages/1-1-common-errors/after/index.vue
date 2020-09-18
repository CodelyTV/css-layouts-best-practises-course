<template>
  <div>
    <Header />
    <main>
      <Hero />
      <Courses />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header'
import Hero from './components/Hero'
import Courses from './components/Courses'
import Footer from '~/common/Footer'

export default {
  components: {
    Header,
    Hero,
    Courses,
    Footer,
  },
}
</script>
