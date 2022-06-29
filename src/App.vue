<template>
  <div data-spy="scroll" id="page-top">
    <component v-bind:is="currentHeader" />
    <router-view />
  </div>
</template>

<script>
import compHeader from "@/components/Header/Header.vue";
import compDashboardHeader from "@/components/Header/DashboardHeader.vue";
export default {
  name: "App",
  components: {
    compHeader,
    compDashboardHeader,
  },
  data() {
    return {
      headers: {
        landing: "compHeader",
        dashboard: "compDashboardHeader",
      },
      currentHeader: "compHeader",
    };
  },
  mounted() {
    window.addEventListener("DOMContentLoaded", () => {
      // Navbar shrink function
      var navbarShrink = function () {
        const navbarCollapsible = document.body.querySelector("#mainNav");
        if (!navbarCollapsible) {
          return;
        }
        if (window.scrollY === 0) {
          navbarCollapsible.classList.remove("navbar-shrink");
        } else {
          navbarCollapsible.classList.add("navbar-shrink");
        }
      };

      // Shrink the navbar
      navbarShrink();

      // Shrink the navbar when page is scrolled
      document.addEventListener("scroll", navbarShrink);
    });
  },
  methods: {},
};
</script>

<style src="./assets/css/styles.css">
</style>
