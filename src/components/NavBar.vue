<template>
  <div class="c-header">
    <Logo />
    <ul class="c-navbar">
      <li>
        <router-link :to="{ name: 'Home' }">Home</router-link>
      </li>
      <li>
        <router-link :to="{ name: 'My Projects' }">My Projects</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
import Logo from "./Logo.vue";

export default {
  name: "NavBar",
  components: {
    Logo,
  },
};
</script>

<style scoped>
.c-header {
  padding: var(--baseline) 0;
}

.c-navbar {
  list-style: none;
  padding: 0 var(--baseline-xl);
}

.c-navbar li {
  display: inline-block;
  margin: var(--baseline-xs) var(--baseline-s);
}

.c-navbar a {
  font-size: 1.4rem;
}
</style>
