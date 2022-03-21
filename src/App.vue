<template>
  <div id="nav">
    <TerminalInfo />
    <TerminalLinks />
  </div>
  <router-view />
</template>

<script>
import TerminalInfo from "@/components/Terminal/TerminalInfo.vue";
import TerminalLinks from "@/components/Terminal/TerminalLinks.vue";

export default {
  name: "HomeView",
  components: {
    TerminalInfo,
    TerminalLinks,
    // HomeView,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&family=Ubuntu+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap");

body {
  background-color: var(--background);
  color: var(--foreground) !important;
  font-family: "IBM Plex Mono", monospace;
  font-size: 22px;
}
::selection {
  background-color: var(--selection_background);
  color: var(--background);
}
::-moz-selection {
  background-color: var(--selection_background);
  color: var(--background);
}
a {
  color: var(--foreground);
  text-decoration-style: dotted;
  text-decoration-thickness: 2px;
  text-underline-offset: 2px;
  text-decoration-line: underline;
  text-underline-position: below;
}
a.router-link-active {
  --color2: var(--color10);
  --color3: var(--color11);
  --color7: var(--color15);
}

/* Remove scrollbars */
::-webkit-scrollbar {
  display: none;
}

:root {
  /* Back and foreground */
  --foreground: #9da5b4;
  --background: #1d1d1d;
  --background-lighter: #2d2d2d;
  --selection_background: #fff;
  /* Black */
  --color0: #2d3139;
  --color8: #bdbdbd;
  /* Red */
  --color1: #f865a5;
  --color9: #b04875;
  /* green */
  --color2: #29edbe;
  --color10: #199175;
  /* Yellow */
  --color3: #ffc457;
  --color11: #9c7835;
  /* blue */
  --color4: #33aeff;
  --color12: #2275ab;
  /* Magenta */
  --color5: #af54ff;
  --color13: #7a3bb3;
  /* Cyan */
  --color6: #2be3fc;
  --color14: #1c95a6;
  /* White */
  --color7: #b3b7bd;
  --color15: #808387;
}
.color0 {
  color: var(--color0);
}
.color8 {
  color: var(--color8);
}
.color1 {
  color: var(--color1);
}
.color9 {
  color: var(--color9);
}
.color2 {
  color: var(--color2);
}
.color10 {
  color: var(--color10);
}
.color3 {
  color: var(--color3);
}
.color11 {
  color: var(--color11);
}
.color4 {
  color: var(--color4);
}
.color12 {
  color: var(--color12);
}
.color5 {
  color: var(--color5);
}
.color13 {
  color: var(--color13);
}
.color6 {
  color: var(--color6);
}
.color14 {
  color: var(--color14);
}
.color7 {
  color: var(--color7);
}
.color15 {
  color: var(--color15);
}
.color0-bg {
  background-color: var(--color0); /* Black */
}
.color8-bg {
  background-color: var(--color8); /* Black */
}
.color1-bg {
  background-color: var(--color1); /* Red */
}
.color9-bg {
  background-color: var(--color9); /* Red */
}
.color2-bg {
  background-color: var(--color2); /* Green */
}
.color10-bg {
  background-color: var(--color10); /* Green */
}
.color3-bg {
  background-color: var(--color3); /* Yellow */
}
.color11-bg {
  background-color: var(--color11); /* Yellow */
}
.color4-bg {
  background-color: var(--color4); /* Blue */
}
.color12-bg {
  background-color: var(--color12); /* Blue */
}
.color5-bg {
  background-color: var(--color5); /* Magenta */
}
.color13-bg {
  background-color: var(--color13); /* Magenta */
}
.color6-bg {
  background-color: var(--color6); /* Cyan */
}
.color14-bg {
  background-color: var(--color14); /* Cyan */
}
.color7-bg {
  background-color: var(--color7); /* White */
}
.color15-bg {
  background-color: var(--color15); /* White */
}
</style>
