<template>
  <section class="hero">
    <div class="hero-content">
      <h1>Cursos para programadores&nbsp;🚀</h1>
      <p>
        Aprende de profesionales con experiencia en cursos prácticos y sin
        rodeos. Mejora tus habilidades, especialízate, y sigue avanzando en tu
        carrera.
      </p>
    </div>
    <figure class="hero-figure">
      <img src="~/assets/images/cursos-codelytv-pro.png" alt="" />
      <figcaption>
        Cursos de principios SOLID, Domain-Driven Design, Arquitectura
        Hexagonal, Docker, CQRS, Microservicios, Kubernetes, Testing y mucho
        más.
      </figcaption>
    </figure>
  </section>
</template>

<style scoped>
.hero {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 0 2rem;
  color: #fff;
}
.hero > * {
  margin: 1rem;
}

.hero-content {
  flex-basis: 0;
  flex-grow: 999;
  min-width: calc(48% - 2rem);
  padding-right: 2rem;
}
.hero-content h1 {
  font-size: 2.7rem;
}
@media (min-width: 32rem) {
  .hero-content h1 {
    font-size: 3.2rem;
  }
}
.hero-content p {
  font-size: 1.5rem;
}

.hero-figure {
  flex-basis: 33rem;
  flex-grow: 1;
  max-width: 33rem;
}
.hero-figure img {
  max-width: 100%;
  margin-bottom: 1rem;
}
</style>
