<template>
  <div class="c-footer">
    <Separator />
    <p class="c-code-block">
      people use typescript for everything, wait 10s to compile on each change,
      and then happily wait to see their portfolio crash because an api returned
      a string instead of an int
    </p>
    <p>
      <span class="c-hightlight">&#169; 2021</span>
      made by
      <a class="c-hightlight" href="https://github.com/Yimura" target="_blank">
        Yimura
      </a>
    </p>
  </div>
</template>

<script>
import Separator from "@/components/Separator.vue";

export default {
  name: "Footer",
  components: {
    Separator,
  },
};
</script>

<style scoped>
.c-code-block {
  font-family: Consolas, "Ubuntu Mono", Ubuntu, monospace;
  padding: 0 var(--baseline-xs);
}

.c-footer {
  margin: 0 auto;
  text-align: center;
  width: 100%;
}
</style>
