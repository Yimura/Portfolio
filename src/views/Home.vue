<template>
  <article class="c-home">
    <h1 class="c-title">
      Hi, my name is <span class="c-hightlight">Andreas Maerten</span> 👋
    </h1>
    <p>I'm a student and free time software developer.</p>
    <div class="c-skillset">
      <h2>My Skillset</h2>
      <div class="c-skillset-wrapper">
        <div class="c-skill"></div>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  name: "Home",
  data: () => {
    return {
      skills: [
        {
          type: "LANGUAGE",
          name: "C++",
          title: "BASIC",
          mastering: 0.15,
        },
        {
          type: "LANGUAGE",
          name: "C#",
          title: "NOVICE",
          mastering: 0.2,
        },
        {
          type: "LANGUAGE",
          name: "CSS / HTML",
          title: "NOVICE",
          mastering: 0.2,
        },
        {
          type: "LANGUAGE",
          name: "JS",
          title: "EXPERT",
          mastering: 0.95,
        },
      ],
    };
  },
};
</script>

<style scoped>
.c-title {
  font-size: var(--baseline-s);
}

.c-title > .c-hightlight {
  font-size: var(--baseline-m);
}

.c-skillset {
  margin: var(--baseline-m) var(--baseline-xl);
}
</style>
