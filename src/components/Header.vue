<template>
  <header>
    <nav class="main_navbar">
      <div class="logo_navbar">
        <img src="../assets/dc-logo.png" alt="DC logo" />
      </div>
      <div class="link_navbar">
        <ul>
          <li
            v-for="(link, i) in linksNavbar"
            :key="i"
            :class="i === currentIndexLink ? 'active' : ''"
          >
            <a href="#" @click.prevent="onActiveNavLink(i)">{{ link.text }}</a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      linksNavbar: [
        {
          text: "Characters",
          href: "#Characters",
        },
        {
          text: "Comics",
          href: "#Comics",
        },
        {
          text: "Movies",
          href: "#Movies",
        },
        {
          text: "Tv",
          href: "#Tv",
        },
        {
          text: "Games",
          href: "#Games",
        },
        {
          text: "Collectibles",
          href: "#Collectibles",
        },
        {
          text: "Videos",
          href: "#Videos",
        },
        {
          text: "Fans",
          href: "#Fans",
        },
        {
          text: "News",
          href: "#News",
        },
        {
          text: "Shop",
          href: "#Shop",
        },
      ],
      currentIndexLink: 1,
    };
  },
  methods: {
    onActiveNavLink(index) {
      this.currentIndexLink = index;
    },
  },
};
</script>

<style>
</style>