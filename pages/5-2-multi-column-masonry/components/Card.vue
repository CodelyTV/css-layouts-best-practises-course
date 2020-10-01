<template>
  <article
    role="button"
    class="card"
    tabindex="0"
    :aria-label="`Ver información del curso ${course.title}`"
    @click="$emit('click')"
  >
    <img class="card-img" :src="`${baseUrl}cursos/${course.img}`" alt="" />
    <div class="card-info">
      <h3>{{ course.title }}</h3>
      <p class="card-lead">
        {{ course.description }}
      </p>
    </div>
  </article>
</template>

<style scoped>
.card {
  min-height: 10rem;
  margin-bottom: 1.5rem;
  background: #fff;
  box-shadow: 0 0.2rem 1rem rgba(0, 0, 0, 0.05);
  cursor: pointer;
  transition: transform 0.3s, box-shadow 0.3s;
  break-inside: avoid;
}
.card:hover,
.card:focus {
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
  transform: translateY(-0.5rem);
}
.card:focus {
  outline: 5px solid var(--primary-color);
}
.card-img {
  width: 100%;
}
.card-info {
  padding: 0 1rem 1rem;
}
</style>

<script>
export default {
  props: {
    course: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      baseUrl: process.env.BASE_PATH || '/',
    }
  },
}
</script>
