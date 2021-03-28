<template>
  <div class="c-footer">
    <Separator />
    <pre>
      <code>people use typescript for everything, wait 10s to compile on each change, and then happily wait to see their portfolio crash because an api returned a string instead of an int</code>
    </pre>
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
.c-footer {
  margin: 0 auto;
  text-align: center;
  width: 100%;
}
</style>
