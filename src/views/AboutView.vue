<template>
  <div class="about">
    <TerminalPrompt dir="~" user="cakes">
      <span class="color0"># I don't know what to put here yet.</span>
    </TerminalPrompt>
  </div>
</template>

<script>
import TerminalPrompt from "@/components/Terminal/TerminalPrompt.vue";

export default {
  name: "AboutView",
  components: {
    TerminalPrompt,
  },
};
</script>
