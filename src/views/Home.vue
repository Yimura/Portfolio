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
          <p>
            {{ skill.description }}
          </p>
        </div>
      </div>
    </div>
    <Separator />
    <div class="c-socials">
      <h1>Socials</h1>
      <ul class="c-socials__list">
        <li v-bind:key="social.url" v-for="social in socials">
          <a v-bind:href="social.url" target="_blank">
            <font-awesome-icon :icon="['fab', social.icon]" />
            {{ social.text }}
          </a>
        </li>
      </ul>
    </div>
  </article>
</template>

<script>
import Separator from "@/components/Separator.vue";

export default {
  name: "Home",
  components: {
    Separator,
  },
  data: () => {
    return {
      skills: [
        {
          type: "LANGUAGE",
          name: "C++",
          title: "BASIC",
          description:
            "Creating modifications for games with DLL injection, simple console applications",
        },
        {
          type: "LANGUAGE",
          name: "C#",
          title: "NOVICE",
          description:
            "Making a REST API with repository/services design, MVC and entity frameworks. ",
        },
        {
          type: "SKILL",
          name: "Docker",
          title: "EXPERT",
          description:
            "Custom image creation and deployment of services with docker-compose.",
        },
        {
          type: "SKILL",
          name: "Fullstack Web",
          title: "NOVICE",
          description:
            "Full stack integration of backend and visualising in an existing design.",
        },
        {
          type: "LANGUAGE",
          name: "NodeJS",
          title: "EXPERT",
          description:
            "NodeJS is my go-to language when I'd like to create a quick script or a general purpose console application.",
        },
        {
          type: "LANGUAGE",
          name: "Lua",
          title: "MODERATE",
          description:
            "I've used this before for scripting some simple game plugins for gmod and FiveM.",
        },
        {
          type: "LANGUAGE",
          name: "PHP",
          title: "MODERATE",
          description:
            "A long time ago I used to create some small MySQL web applications but haven't touched it in a while.",
        },
        {
          type: "LANGUAGE",
          name: "Python",
          title: "MODERATE",
          description:
            "Won't use this language unless specifically required for the task.",
        },
        {
          type: "FRAMEWORK",
          name: "VueJS",
          title: "BASIC",
          description: "This website was made with VueJS.",
        },
      ],
      socials: [
        {
          icon: "discord",
          text: "Yimura#6969",
          url: "#",
        },
        {
          icon: "github",
          text: "Github",
          url: "http://github.com/Yimura",
        },
        {
          icon: "twitch",
          text: "Twitch",
          url: "https://twitch.tv/yimura_",
        },
        {
          icon: "twitter",
          text: "Twitter",
          url: "https://twitter.com/Yimura9",
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
  white-space: nowrap;
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

.c-socials {
  text-align: center;
  margin: var(--baseline-l) 0;
}

.c-socials__list {
  list-style: none;
}

.c-socials__list li {
  margin-bottom: var(--baseline);
}
</style>
