<template>
  <div id="app">
    <NavBar />
    <div class="c-content">
      <router-view />
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from "@/components/Footer.vue";
import NavBar from "@/components/NavBar.vue";

export default {
  components: {
    Footer,
    NavBar,
  },
};
</script>

<style>
:root {
  --baseline: calc(1rem / 2);
  --baseline-xs: calc(var(--baseline) * 2);
  --baseline-s: calc(var(--baseline) * 3);
  --baseline-m: calc(var(--baseline) * 4);
  --baseline-l: calc(var(--baseline) * 5);
  --baseline-xl: calc(var(--baseline) * 6);

  --steel-gray: #1e1d2c;
  --royal-blue: #2c61e8;
  --gray-suit: #cac8d3;
  --danube: #71a7d1;

  --header-height: 8rem;
  --footer-height: 0;
  --content-height: calc(100vh - var(--header-height) - var(--footer-height));
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

body {
  background-color: var(--steel-gray);
  color: var(--gray-suit);
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  font-size: var(--baseline-xs);
  line-height: 1.5;
}

h1,
h2,
h3,
h4,
h5,
p {
  margin-bottom: var(--baseline);
}

progress {
  -webkit-appearance: none;
  appearance: none;
  border-radius: 3px;
  height: 10px;
  overflow: hidden;
  width: 100%;
}

progress::-webkit-progress-bar {
  background-color: var(--gray-suit);
}

progress::-webkit-progress-value {
  background-color: var(--royal-blue);
}

a {
  color: var(--gray-suit);
  text-decoration: none;
  transition: 300ms ease-out;
}

a:hover,
a.router-link-exact-active {
  color: var(--royal-blue);
  transition: 150ms ease-in;
}

#app {
  width: 100vw;
  height: 100vh;
}

.c-header {
  height: var(--header-height);
}

.c-content {
  height: var(--content-height);
  overflow: auto;
  padding: var(--baseline-s) 0;
  width: 100%;
}

.c-content > * {
  margin: 0 auto;
  width: 90%;
}

.c-footer {
  height: var(--footer-height);
}

.c-hightlight {
  color: var(--royal-blue);
}

/**
 * Normal Screens
 */
@media only screen and (min-width: 960px) and (min-height: 500px) {
  :root {
    --footer-height: 6.4rem;
  }

  .c-navbar {
    display: unset !important;
    justify-content: unset !important;
  }

  .c-content > * {
    width: 60%;
  }
}

/**
 * Ultrawide resolutions
 */
@media only screen and (min-width: 2000px) and (min-height: 1100px) {
  .c-content > * {
    width: 40%;
  }
}
</style>
