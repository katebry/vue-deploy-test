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
  data: function() {
    return {
      books: [
        {
          title: "Nevada",
          rating: "4.5",
          imageName: "nevada",
          imageAlt: "Nevada book cover",
          scores: {
            kate: "3",
            neal: "5",
            gg: "6.5",
            clinch: "5",
            tim: "N/A",
            charlotte: "N/A",
          },
        },
        {
          title: "One Day in the Life of Ivan Denisovich",
          rating: "7.4",
          imageName: "ivanDenisovich",
          imageAlt: "One Day in the Life of Ivan Denisovich book cover",
          scores: {
            kate: "10",
            neal: "9",
            gg: "3",
            clinch: "7",
            tim: "8",
            charlotte: "N/A",
          },
        },
        {
          title: "Stonefish",
          rating: "3.9",
          imageName: 'stonefish',
          imageAlt: 'Stonefish book cover',
          scores: {
            kate: "1.5",
            neal: "4",
            gg: "5",
            clinch: "N/A",
            tim: "5",
            charlotte: "N/A",
          },
        },
        {
          title: "The Haunting of Hill House",
          rating: "8.4",
          imageName: 'hauntingOfHH',
          imageAlt: 'The Haunting of Hill House book cover',
          scores: {
            kate: "8",
            neal: "10",
            gg: "N/A",
            clinch: "7",
            tim: "8",
            charlotte: "9",
          },
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
