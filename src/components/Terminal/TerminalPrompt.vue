<template>
  <div class="prompt">
    <span class="prompt-text">
      <span class="prompt-user">{{ user }}</span>
      <span class="prompt-separator"></span>
      <span class="prompt-dir">{{ dir }}</span>
      <span class="prompt-shebang">❯</span>
      <span class="prompt-command"><slot></slot></span>
    </span>
  </div>
</template>

<script>
export default {
  name: "TerminalPrompt",
  props: {
    user: String,
    path: String,
    dir: String,
  },
};
</script>

<style scoped>
.prompt {
  display: flex;
  align-items: center;
  padding: 5px;
  font-size: 22px;
  color: var(--color1);
}

.prompt-text {
  display: flex;
  align-items: center;
}

.prompt-user {
  font-weight: bold;
}

.prompt-path {
  font-weight: bold;
}

.prompt-dir {
  color: var(--color3);
}

.prompt-separator {
  margin-left: 5px;
  margin-right: 5px;
}

.prompt-shebang {
  color: var(--color3);
  margin-left: 10px;
}

.prompt-command {
  color: var(--color4);
  margin-left: 10px;
}
</style>
