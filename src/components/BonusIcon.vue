<template>
  <div class="info_footer">
    <ul>
      <li v-for="(link, i) in linksInfoFooter" :key="i">
        <img :src="require('../assets/' + link.src)" alt="info logo" />
        <a href="#">{{ link.text }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "BonusIcon",
  data() {
    return {
      linksInfoFooter: [
        {
          text: "Digital comics",
          src: "buy-comics-digital-comics.png",
        },
        {
          text: "Dc merchandise",
          src: "buy-comics-merchandise.png",
        },
        {
          text: "Subscription",
          src: "buy-comics-subscriptions.png",
        },
        {
          text: "Comic shop locator",
          src: "buy-comics-shop-locator.png",
        },
        {
          text: "Dc power visa",
          src: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<style>
</style>