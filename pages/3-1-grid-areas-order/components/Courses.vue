<template>
  <div class="block">
    <section class="courses">
      <h2 class="courses-title">👌 Cursos disponibles</h2>
      <Filters class="courses-filters" />
      <div class="courses-collection">
        <Card v-for="course in courses" :key="course.title" :course="course" />
      </div>
    </section>
  </div>
</template>

<style scoped>
.block {
  background: #eee;
}

.courses {
  display: grid;
  grid-template-areas:
    'title   title   title   title'
    'content content content sidebar'
    'content content content sidebar';
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 4rem 1rem;
  column-gap: 2rem;
}
.courses-title {
  grid-area: title;
  font-size: 2rem;
}
.courses-collection {
  display: grid;
  grid-area: content;
  grid-template-columns: repeat(auto-fill, minmax(18rem, 1fr));
  gap: 1.5rem;
}
.courses-filters {
  grid-area: sidebar;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>

<script>
import Card from './Card'
import Filters from './Filters'
import courses from '~/content/courses.json'

export default {
  components: {
    Card,
    Filters,
  },
  data() {
    return {
      courses,
    }
  },
}
</script>
