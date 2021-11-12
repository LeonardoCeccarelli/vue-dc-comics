<template>
  <main>
    <div class="hero_image"><img src="../assets/jumbotron.jpg" alt="" /></div>
    <div class="main_container">
      <div class="title_card_container">
        <h3>Current series</h3>
      </div>
      <div class="card_container">
        <ComicCard
          v-for="(card, i) in listCardDc"
          :key="i"
          :urlCard="card.thumb"
          :title="card.series"
        ></ComicCard>
      </div>
      <div class="btn_container">
        <button type="button">LOAD MORE!</button>
      </div>
    </div>
  </main>
</template>

<script>
import dcComics from "../database/dc-comics.json";
import ComicCard from "./ComicCard.vue";
export default {
  name: "Main",
  components: {
    ComicCard,
  },
  data() {
    return {
      listCardDc: dcComics,
    };
  },
};
</script>

<style>
</style>