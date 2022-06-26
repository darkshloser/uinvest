<template>
  <header class="p-3 bg-dark text-white">
    <div class="container">
      <div
        class="d-flex flex-wrap align-items-center justify-content-center justify-content-lg-start"
      >
        <a
          href="/"
          class="d-flex align-items-center mb-2 mb-lg-0 text-white text-decoration-none"
        >
          <svg
            class="bi me-2"
            width="40"
            height="32"
            role="img"
            aria-label="Bootstrap"
          >
            <use xlink:href="#bootstrap" />
          </svg>
        </a>

        <ul
          class="nav col-12 col-lg-auto me-lg-auto mb-2 justify-content-center mb-md-0"
        >
          <li class="nav-item">
            <router-link
              class="nav-link px-2 text-white"
              aria-current="page"
              to="/"
              >Home</router-link
            >
          </li>
          <li class="nav-item">
            <router-link
              class="nav-link px-2 text-white"
              aria-current="page"
              to="/about"
              >About</router-link
            >
          </li>
        </ul>

        <div class="text-end">
          <button type="button" class="btn btn-outline-light me-2">
            Login
          </button>
          <button type="button" class="btn btn-warning">Sign-up</button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  component: {},
  data() {
    return {};
  },
};
</script>

<style scoped>
</style>