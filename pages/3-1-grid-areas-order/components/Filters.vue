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
  flex-direction: column;
  flex-wrap: wrap;
  max-width: var(--max-width);
}

.filters-tags {
  display: flex;
  flex-direction: column;
  order: 1;
  margin: 0 auto 0 -0.5rem;
  padding: 0.5rem;
  list-style: none;
  row-gap: 0.5rem;
}

.search {
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
