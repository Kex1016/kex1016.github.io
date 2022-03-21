<template>
  <div class="home">
    <TerminalPrompt dir="~" user="cakes">
      <span class="color0"># This is the end of the page.</span>
    </TerminalPrompt>
  </div>
</template>

<script>
import TerminalPrompt from "@/components/Terminal/TerminalPrompt.vue";

export default {
  name: "HomeView",
  components: {
    TerminalPrompt,
  },
};
</script>
