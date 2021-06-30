<template>
  <particles-bg num="10" type="tadpole" />
  <h1>{{ msg }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { ParticlesBg } from "particles-bg-vue";

export default defineComponent({
  name: "Title",
  components: {
    ParticlesBg,
  },
  props: {
    msg: String,
  },
});
</script>

<style scoped>
h1 {
  color: #e63f80;
  position: absolute;
  font-size: 50px;
  top: 25px;
  left: 0;
  right: 0;
}
</style>
