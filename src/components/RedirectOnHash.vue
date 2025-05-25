<template>
  <!-- This component renders nothing; it's only for redirection logic -->
</template>

<script>
export default {
  name: "RedirectOnHash",
  mounted() {
    if (typeof window !== "undefined") {
      const hash = window.location.hash;
      const legacyHashes = [
        "#usage-with-v-model",
        "#v-model-arguments",
        "#multiple-v-model-bindings",
        "#handling-v-model-modifiers",
      ];

      if (legacyHashes.includes(hash)) {
        window.location = "./v-model.html" + hash;
      }
    }
  },
};
</script>
