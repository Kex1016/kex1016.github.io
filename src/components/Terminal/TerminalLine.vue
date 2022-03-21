<template>
  <div class="line">
    <div class="line-content" v-if="!isSeparator">
      <img class="line-content-icon" v-if="icon && !iconText" :src="icon" />
      <span class="line-content-icon" v-if="iconText">{{ iconText }}</span>
      <span class="line-content-text"><slot></slot></span>
    </div>
    <div class="line-separator" v-if="isSeparator"></div>
  </div>
</template>

<script>
export default {
  name: "TerminalLine",
  props: {
    icon: String,
    iconText: String,
    text: String,
    isSeparator: Boolean,
  },
};
</script>

<style scoped>
.line-content {
  display: flex;
  align-items: center;
}

.line-content-icon {
  width: 25px;
  height: 25px;
  margin-right: 10px;
}

.line-separator {
  width: calc(100% + 20px);
  height: 5px;
  background-color: var(--color4);
  border-radius: 0;
}
</style>
