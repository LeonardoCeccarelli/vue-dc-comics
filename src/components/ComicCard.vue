<template>
  <div class="single_card_container">
    <div class="single_card">
      <img :src="urlCard" alt="logo card" />
      <h5>{{ title }}</h5>
    </div>
  </div>
</template>

<script>
export default {
  name: "ComicCard",
  props: {
    urlCard: String,
    title: String,
    price: String,
    type: String,
  },
};
</script>

<style>
</style>