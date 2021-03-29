<template>
  <article class="c-home">
    <h1 class="c-title">
      Hi, my name is <span class="c-hightlight">Andreas Maerten</span> 👋
    </h1>
    <p>I'm a student and free time software developer.</p>
    <div class="c-skillset">
      <h2>My Skillset</h2>
      <div class="c-skillset-wrapper">
        <div class="c-skill" v-bind:key="skill.name" v-for="skill in skills">
          <div class="c-skill__head">
            <h1>{{ skill.name }}</h1>
            <div>
              <span class="c-skill__tag">{{ skill.type }}</span>
            </div>
          </div>
          <progress
            v-bind:title="skill.title"
            v-bind:value="skill.mastering"
            max="1"
          />
        </div>
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
          mastering: 0.35,
        },
        {
          type: "LANGUAGE",
          name: "CSS / HTML",
          title: "MODERATE",
          mastering: 0.75,
        },
        {
          type: "LANGUAGE",
          name: "JS",
          title: "EXPERT",
          mastering: 0.95,
        },
        {
          type: "LANGUAGE",
          name: "Lua",
          title: "MODERATE",
          mastering: 0.45,
        },
        {
          type: "LANGUAGE",
          name: "PHP",
          title: "MODERATE",
          mastering: 0.55,
        },
        {
          type: "LANGUAGE",
          name: "Python",
          title: "MODERATE",
          mastering: 0.65,
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

.c-skillset-wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  margin: 0 calc(-1 * var(--baseline-xl));
}

.c-skill {
  border: 1px solid var(--gray-suit);
  border-radius: calc(var(--baseline) / 2);
  margin: 0 var(--baseline-xs) var(--baseline-s);
  min-width: 300px;
  padding: var(--baseline) var(--baseline-xs);
}

.c-skill__head {
  display: flex;
}

.c-skill__head > h1 {
  flex-grow: 1;
}

.c-skill__tag {
  background-color: var(--gray-suit);
  border-radius: var(--baseline-xs);
  color: var(--steel-gray);
  font-size: 14px;
  font-weight: bold;
  padding: 2px 8px;
}
</style>
