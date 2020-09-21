<template>
  <section class="filters">
    <ul class="filters-tags">
      <li v-for="filter in filters" :key="filter">
        <Checkbox :value="filter" />
      </li>
    </ul>
    <label for="search" class="sr-only">Buscar</label>
    <input id="search" type="search" placeholder="Buscar…" class="search" />
  </section>
</template>

<style scoped>
.filters {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  max-width: var(--max-width);
  margin: 2rem auto;
}

.filters-tags {
  display: flex;
  flex-grow: 1;
  margin: 0 auto 0 -0.5rem;
  padding: 0.5rem;
  overflow: auto;
  column-gap: 0.2rem;
  list-style: none;
  mask-image: linear-gradient(to left, transparent 1%, black 13%);
}

.search {
  flex-basis: 0;
  flex-grow: 1;
  padding: 0.3rem 0.5rem;
  font-size: 1rem;
  border: 1px solid transparent;
}
.search:focus {
  border: 1px solid var(--primary-color);
  outline: 2px solid var(--primary-color);
}
</style>

<script>
import Checkbox from '~/common/Checkbox'

export default {
  components: {
    Checkbox,
  },
  data() {
    return {
      activeFilters: [],
      filters: [
        'Arquitectura',
        'DevOps',
        'Tooling',
        'Backend',
        'JavaScript',
        'Mobile',
      ],
    }
  },
}
</script>
