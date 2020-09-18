<template>
  <article
    role="button"
    class="card"
    tabindex="0"
    :aria-label="`Ver información del curso ${course.title}`"
    @click="$emit('click')"
  >
    <img class="card-img" :src="`/cursos/${course.img}`" alt="" />
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
  background: #fff;
  box-shadow: 0 0.2rem 1rem rgba(0, 0, 0, 0.05);
  transition: transform 0.3s, box-shadow 0.3s;
}
.card-info {
  padding: 0 1rem 1rem;
}
.card-img {
  width: 100%;
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
}
</script>
