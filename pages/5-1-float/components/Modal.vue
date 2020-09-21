<template>
  <div class="modal-backdrop" @click="close">
    <section class="modal" @click.stop>
      <button aria-label="Cerrar" class="modal-close" @click="close">
        &times;
      </button>
      <slot />
    </section>
  </div>
</template>

<style scoped>
.modal-backdrop {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
}
.modal {
  position: relative;
  min-width: 85vw;
  max-height: 100vh;
  padding: 4rem 1vw;
  overflow: auto;
  background: #fff;
  box-shadow: 0 0 1rem #000;
}
.modal-close {
  position: absolute;
  top: 1rem;
  right: 1rem;
  margin: 0;
  padding: 0 1rem;
  font-size: 2rem;
  background: transparent;
  border: none;
  cursor: pointer;
}
.modal-close:focus {
  outline: 2px solid var(--primary-color);
}
</style>

<script>
export default {
  mounted() {
    document.addEventListener('keydown', this.handleKeyDown)
  },
  beforeDestroy() {
    document.removeEventListener('keydown', this.handleKeyDown)
  },
  methods: {
    close() {
      this.$emit('close')
    },
    handleKeyDown({ key }) {
      if (key === 'Escape') {
        this.close()
      }
    },
  },
}
</script>
