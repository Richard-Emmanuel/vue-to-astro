<!-- src/components/MouseTracker.vue -->
<template>
  <div class="mouse-area">
    <div class="mouse-card">
      <p><strong>X:</strong> {{ x }}</p>
      <p><strong>Y:</strong> {{ y }}</p>
    </div>
  </div>
</template>

<script setup>
import { useMouse } from "../components/useMouse";

const { x, y } = useMouse();
</script>

<style scoped>
.mouse-area {
  width: 100%;
  height: 100vh;
  position: relative;
}

.mouse-card {
  position: fixed;
  top: 1rem;
  right: 1rem;
  background-color: white;
  border: 1px solid #ddd;
  padding: 1rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  font-family: sans-serif;
}
</style>
