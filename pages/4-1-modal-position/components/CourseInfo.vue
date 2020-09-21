<template>
  <section class="course-content">
    <h2 class="course-content-title">Domain-Driven Design - DDD Aplicado</h2>
    <p class="course-content-lead">
      Aprende a modelar tus aplicaciones centrándote en tu dominio, definir
      Bounded Contexts, agregados, value objects, y mucho más. Todo de forma
      práctica y con ejemplos de código ⚡
    </p>

    <h3>💸 ¡Primera lección disponible sin registro!</h3>
    <p>
      En el curso de Event-Driven Architecture analizamos cómo se comunican los
      distintos servicios de nuestra empresa, pero… ¿Cómo modelamos los
      servicios y aplicaciones de nuestra empresa?
    </p>

    <p>
      Si queremos modelar un sistema complejo necesitamos complementar
      principios y técnicas como los principios SOLID o la Arquitectura
      Hexagonal con una parte estratégica. Es ahí donde entra Domain-Driven
      Design (DDD).
    </p>

    <p>
      DDD hace de paraguas agrupando toda una serie de conceptos a nivel técnico
      y estratégico para promover:
    </p>

    <ul>
      <li>
        Colaboración entre negocio o producto y el equipo técnico para modelar
        en código los problemas particulares de un determinado dominio (Bounded
        Contexts, Ubiquitous Language, Agregados, Value Objects, Eventos de
        Dominio, Entidades, Repositorios…)
      </li>
      <li>
        Poner el foco de nuestra aplicación en el dominio. Manteniendo una alta
        tolerancia al cambio y evolución de los sistemas a lo largo del tiempo
      </li>
      <li>
        Alta testabilidad de nuestra lógica de negocio gracias a desacoplarnos
        de la infraestructura
      </li>
      <li>Facilitar la colaboración entre distintos equipos de desarrollo</li>
    </ul>
  </section>
</template>

<style scoped>
.course-content {
  max-width: 90ch;
  margin: 0 auto;
  padding: 0 4rem;
  font-size: 1.2rem;
}
.course-content h3 {
  font-size: 1.7rem;
}
.course-content-title {
  font-size: 2.7rem;
}
.course-content-lead {
  margin-bottom: 4rem;
  padding-bottom: 2rem;
  color: rgba(0, 0, 0, 0.7);
  font-size: 1.5rem;
  font-family: var(--ff-primary);
  line-height: 1.3;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}
</style>
