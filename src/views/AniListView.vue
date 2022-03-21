<template>
  <div class="anilist">
    <TerminalPrompt dir="~" user="cakes">
      <span class="color12">cd </span>
      <span class="color4">~/anilist</span>
    </TerminalPrompt>
    <TerminalPrompt dir="~/anilist" user="cakes">
      <span class="color12">cat </span>
      <span class="color4">~/css.md</span>
    </TerminalPrompt>
    <CSSList />
    <TerminalPrompt dir="~/anilist" user="cakes">
      <span class="color0"># This is the end of the page.</span>
    </TerminalPrompt>
  </div>
</template>

<script>
import TerminalPrompt from "@/components/Terminal/TerminalPrompt.vue";
import CSSList from "@/components/AniList/CSSList.vue";

export default {
  name: "AniListView",
  components: {
    TerminalPrompt,
    CSSList,
  },
};
</script>
