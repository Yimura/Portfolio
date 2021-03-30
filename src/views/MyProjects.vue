<template>
  <div class="c-projects-wrapper">
    <div
      class="c-project"
      v-bind:key="project.title"
      v-for="project in projects"
    >
      <h2 class="c-project__title">{{ project.title }}</h2>
      <p class="c-project__short">{{ project.short }}</p>
      <div class="c-project__links" v-if="project.links">
        <a
          class="c-project__site"
          target="_blank"
          v-bind:key="link.url"
          v-for="link in project.links"
          v-bind:href="link.url"
        >
          {{ link.text }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data: () => {
    return {
      projects: [
        {
          title: "Damon Music",
          short:
            "A music bot aiming to provide a better user experience on Discord than the competition.",
          links: [
            {
              text: "WEBSITE",
              url: "https://music.damon.sh",
            },
          ],
        },
        {
          title: "Damon's Base",
          short:
            "A Discord.js framework/base code to manage modular code and commands.",
          links: [
            {
              text: "SOURCE",
              url: "https://github.com/Damon-Org/damon-base",
            },
          ],
        },
        {
          title: "Import Dir",
          short:
            "A NodeJS ESModule package made to import a directory structure into an object.",
          links: [
            {
              text: "NPMJS",
              url: "https://www.npmjs.com/package/@yimura/import-dir",
            },
            {
              text: "SOURCE",
              url: "https://github.com/Yimura/importDir",
            },
          ],
        },
        {
          title: "Soft & Wet",
          short:
            "A Jojo themed bot with many fun commands, image manipulation and much more!",
          links: [
            {
              text: "SOURCE",
              url: "https://github.com/Soft-Wet-Bot/base",
            },
            {
              text: "WEBSITE",
              url: "https://soft-wet.damon.sh",
            },
          ],
        },
        {
          title: "YouTube DL",
          short:
            "A YouTube video downloader with included conversion to MP3, OGG and WAV file formats.",
          links: [
            {
              text: "DOCKER",
              url: "https://hub.docker.com/yimura/ytdl",
            },
            {
              text: "SOURCE",
              url: "https://github.com/Yimura/node-ytdl-gui",
            },
            {
              text: "WEBSITE",
              url: "https://ytdl.pieceof.art",
            },
          ],
        },
        {
          title: "YTScraper",
          short:
            "Lightweight, widely supported and fast YT search scraper with support for channel, stream and video search.",
          links: [
            {
              text: "NPMJS",
              url: "https://www.npmjs.com/package/@yimura/scraper",
            },
            {
              text: "SOURCE",
              url: "https://github.com/Yimura/Scraper",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.c-projects-wrapper {
  display: grid;
  column-gap: var(--baseline-m);
  row-gap: var(--baseline-s);
  grid-template-columns: repeat(3, 1fr);
}

.c-project {
  border: 1px solid var(--gray-suit);
  border-radius: calc(var(--baseline) / 2);
  display: flex;
  flex-direction: column;
  padding: var(--baseline-s) var(--baseline-m);
}

.c-project__title {
  color: var(--royal-blue);
  margin-bottom: var(--baseline);
}

.c-project__short {
  flex-grow: 1;
}

.c-project__links {
  display: flex;
  margin: calc(-1 * var(--baseline));
  margin-top: 0;
}

.c-project__site {
  padding: var(--baseline);
}
</style>
