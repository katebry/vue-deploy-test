<template>
  <div class="container">
    <div class="content">
      <h2>{{ title }}</h2>
      <img
        :src="require(`@/assets/bookCovers/${this.imageName}.jpg`)"
        :alt="this.imageAlt"
      />
      <div class="btn-wrapper">
        <button @click="toggleRatings">
          {{ ratingsVisible ? "Hide Average Rating" : "Show Average Rating" }}
        </button>
      </div>
      <h1 v-if="this.ratingsVisible">{{ rating }}</h1>
      <p v-if="this.ratingsVisible">
        <Ratings :scores="scores" />
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Ratings from "./Ratings.vue";

export default defineComponent({
  components: {
    Ratings,
  },
  name: "Book",
  props: {
    title: {
      type: String,
      required: true,
    },
    rating: {
      type: String,
      required: true,
    },
    imageName: String,
    imageAlt: String,
    scores: Object,
  },
  data: function() {
    return {
      ratingsVisible: false,
    };
  },
  methods: {
    toggleRatings() {
      this.ratingsVisible = !this.ratingsVisible;
    },
  },
});
</script>

<style>
button {
  background-color: #e63f80;
  color: white;
  font-family: Avaline Script;
  font-size: 24px;
  padding: 10px;
  border-radius: 20px;
}
div .container {
  display: flex;
  justify-content: center;
  align-content: center;
}
div .content {
  display: flex;
  flex-direction: column;
}
div .btn-wrapper {
  display: flex;
  justify-content: center;
  align-content: center;
  padding: 15px;
}
img {
  min-width: 300px;
  min-height: 475px;
}
</style>
