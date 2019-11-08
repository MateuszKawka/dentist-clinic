<template>
  <div class="container">
    <header class="header">
      <h1 class="header__logo">Dentist Clinic</h1>
      <Navigation :navLinks="navLinks" :visible="menuVisible" @linkClicked="linkClicked" />
      <div id="nav-icon3" @click="menuBind" :class="{'open': menuVisible}">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>
    </header>
    <main class="main">
      <nuxt />
    </main>
    <Footer />
    <svg width="0" height="0" class="hidden">
      <symbol viewBox="0 0 8 12" xmlns="http://www.w3.org/2000/svg" id="1208065781571662045">
        <title>keyboard_arrow_right</title>
        <g fill="none" fill-rule="evenodd">
          <path d="M-8-6h24v24H-8z" />
          <path fill="#1D1D1D" d="M.59 10.59L5.17 6 .59 1.41 2 0l6 6-6 6z" />
        </g>
      </symbol>
    </svg>
      
  </div>
</template>

<script>
import Navigation from "@/components/layoutComponents/Navigation";
import Footer from "@/components/layoutComponents/Footer";
export default {
  name: "defaultLayout",
  components: {
    Navigation,
    Footer
  },
  data() {
    return {
      navLinks: [
        {
          name: "Start",
          href: "#start"
        },
        {
          name: "Booking",
          href: "#booking"
        },
        {
          name: "Clinic",
          href: "#clinic"
        },
        {
          name: "Price list",
          href: "#pricing"
        },
        {
          name: "Team",
          href: "#team"
        },
        {
          name: "Blog",
          href: "#blog"
        }
      ],
      menuVisible: false
    };
  },
  methods: {
    menuBind() {
      this.menuVisible = !this.menuVisible;
    },
    linkClicked() {
      this.menuBind();
    }
  }
};
</script>