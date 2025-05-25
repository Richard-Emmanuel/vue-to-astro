<template>
  <div class="demo counter">
    <button @click="count++">Count is: {{ count }}</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const count = ref(0);
</script>
