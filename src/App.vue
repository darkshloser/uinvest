<template>
  <component v-bind:is="currentHeader" />
  <component v-bind:is="headers['dashboard']" />
  <router-view />
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
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
