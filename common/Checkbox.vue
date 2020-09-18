<template>
  <div :for="value" class="toggle">
    <input :id="value" :value="value" type="checkbox" />
    <label :for="value" class="toggle-label">
      {{ value }}
    </label>
  </div>
</template>

<style scoped>
.toggle {
  position: relative;
}
.toggle-label {
  display: inline-block;
  padding: 0.5rem 1rem;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 1.2rem;
  cursor: pointer;
  transition: background 0.2s, color 0.2s;
}
.toggle-label:hover {
  background: rgba(0, 0, 0, 0.1);
}
.toggle input {
  position: absolute;
  opacity: 0;
}
.toggle input:focus + .toggle-label {
  box-shadow: 0 0 0 0.2rem var(--primary-color);
}
.toggle input:checked + .toggle-label {
  color: #fff;
  background: rgba(0, 0, 0, 0.7);
}
</style>

<script>
export default {
  props: {
    value: {
      type: String,
      required: true,
    },
  },
}
</script>
