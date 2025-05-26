<!-- src/components/ModalExample.vue -->
<template>
  <div class="demo">
    <button @click="open = true">Open Modal</button>
    <ClientOnly>
      <teleport to="body">
        <div v-if="open" class="demo modal-demo">
          <p style="margin-bottom: 20px">Hello from the modal!</p>
          <button @click="open = false">Close</button>
        </div>
      </teleport>
    </ClientOnly>
  </div>
</template>

<script setup>
import { ref } from "vue";
const open = ref(false);
</script>

<style scoped>
.modal-demo {
  position: fixed;
  z-index: 999;
  top: 20%;
  left: 50%;
  width: 300px;
  margin-left: -150px;
  background-color: var(--vt-c-bg);
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}
</style>
