<template>
  <div class="title-container">
    <Title msg="Book Club" />
  </div>
  <Book
    v-for="book in books"
    :key="book.title"
    :title="book.title"
    :rating="book.rating"
    :imageName="book.imageName"
    :imageAlt="book.imageAlt"
    :scores="book.scores"
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Title from "./components/Title.vue";
import Book from "./components/Book.vue";

export default defineComponent({
  name: "App",
  components: {
    Title,
    Book,
  },
  data() {
    return {
      books: [
        {
          title: "Nevada",
          rating: "4.5",
          imageName: "nevada",
          imageAlt: "Nevada book cover",
          scores: [
            { name: "kate", score: "3" },
            { name: "neal", score: "5" },
            { name: "gg", score: "6.5" },
            { name: "clinch", score: "5" },
            { name: "tim", score: "N/A" },
            { name: "charlotte", score: "N/A" },
          ],
        },
        {
          title: "One Day in the Life of Ivan Denisovich",
          rating: "7.4",
          imageName: "ivanDenisovich",
          imageAlt: "One Day in the Life of Ivan Denisovich book cover",
          scores: [
            { name: "kate", score: "10" },
            { name: "neal", score: "9" },
            { name: "gg", score: "3" },
            { name: "clinch", score: "7" },
            { name: "tim", score: "8" },
            { name: "charlotte", score: "N/A" },
          ],
        },
        {
          title: "Stonefish",
          rating: "3.9",
          imageName: "stonefish",
          imageAlt: "Stonefish book cover",
          scores: [
            { name: "kate", score: "1.5" },
            { name: "neal", score: "4" },
            { name: "gg", score: "5" },
            { name: "clinch", score: "N/A" },
            { name: "tim", score: "5" },
            { name: "charlotte", score: "N/A" },
          ],
        },
        {
          title: "The Haunting of Hill House",
          rating: "8.4",
          imageName: "hauntingOfHH",
          imageAlt: "The Haunting of Hill House book cover",
          scores: [
            { name: "kate", score: "8" },
            { name: "neal", score: "10" },
            { name: "gg", score: "N/A" },
            { name: "clinch", score: "7" },
            { name: "tim", score: "8" },
            { name: "charlotte", score: "9" },
          ],
        },
      ],
    };
  },
});
</script>

<style>
@font-face {
  font-family: "Avaline Script";
  src: local("Avaline Script Sketch"),
    url("./assets/fonts/Avaline-Script-Sketch.ttf") format("truetype");
}
#app {
  font-family: Avaline Script;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fb7507;
  font-size: 26px;
}
div .title-container {
  width: 100%;
  height: 13vh;
  padding: 20px;
}
</style>
