<template>
  <p>{{ name }} : {{ score }}</p>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Ratings",
  props: {
    score: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },
});
</script>

<style scoped>
div {
  letter-spacing: 2px;
}
</style>
