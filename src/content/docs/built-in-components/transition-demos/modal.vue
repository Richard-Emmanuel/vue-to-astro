<template>
  <div>
    <button @click="openModal = true">Open Modal</button>

    <teleport to="body">
      <div v-if="openModal" class="modal-overlay" @click.self="closeModal">
        <div class="modal-content">
          <p class="card">Hello from the Modal!</p>
          <button @click="closeModal">Close</button>
        </div>
      </div>
    </teleport>
  </div>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return {
      openModal: false,
    };
  },
  methods: {
    closeModal() {
      this.openModal = false;
    },
  },
};
</script>

<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;
  background-color: rgba(0, 0, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

.modal-content {
  background: var(--vt-c-bg-mute);
  padding: 2rem;
  border-radius: 8px;
  min-width: 300px;
}
</style>
