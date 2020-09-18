<template>
  <main class="index">
    <h1>CSS Layouts best practises course</h1>
    <ul>
      <li>
        <nuxt-link to="/1-1-common-errors/after">Common errors</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/1-2-units">Units</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/2-1-responsive-flex">Responsive with Flex</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/2-2-responsive-grid">Responsive with Grid</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/3-1-grid-areas-order">Grid Areas and order</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/4-1-modal-position">
          A Modal with position absolute, relative and fixed
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/4-2-menu-sticky">A Menu with position sticky</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/4-3-understanding-z-index">
          Understanding z-index
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/5-1-float">Float without clearfix</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/5-2-multi-column-masonry">
          Multi-column masonry
        </nuxt-link>
      </li>
    </ul>
  </main>
</template>

<style scoped>
.index {
  width: 100%;
  min-height: 100vh;
  padding: 2rem;
  background: #fff;
}
</style>
