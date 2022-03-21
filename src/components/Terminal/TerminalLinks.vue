<template>
  <div class="nav">
    <TerminalPrompt dir="~" user="cakes"
      ><span class="color12">cat </span>
      <span class="color4">navigation.md</span></TerminalPrompt
    >
    <div class="links">
      <router-link to="/">
        <span class="color2">[</span>
        <span class="color7">home</span>
        <span class="color2">]</span>
        <span class="color3">(</span>
        <span class="color7">/</span>
        <span class="color3">)</span>
      </router-link>
      <router-link to="/about">
        <span class="color2">[</span>
        <span class="color7">about</span>
        <span class="color2">]</span>
        <span class="color3">(</span>
        <span class="color7">/about</span>
        <span class="color3">)</span>
      </router-link>
      <router-link to="/anilist">
        <span class="color2">[</span>
        <span class="color7">anilist</span>
        <span class="color2">]</span>
        <span class="color3">(</span>
        <span class="color7">/anilist</span>
        <span class="color3">)</span>
      </router-link>
    </div>
  </div>
</template>

<script>
import TerminalPrompt from "@/components/Terminal/TerminalPrompt.vue";

export default {
  name: "TerminalLinks",
  components: {
    TerminalPrompt,
  },
};
</script>

<style scoped>
.links {
  margin-top: 5px;
  margin-bottom: 10px;
}
a {
  color: var(--color4);
  margin-left: 10px;
  text-decoration-color: var(--color15);
}
</style>
