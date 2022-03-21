<template>
  <div class="container">
    <div class="terminal-image">
      <img src="./Images/logo.gif" alt="Logo?" />
    </div>
    <div class="terminal-text">
      <TerminalLine class="component terminal-text-title"
        >kex1016<span class="color1">@</span>github.io</TerminalLine
      >
      <TerminalLine
        class="component terminal-text-separator"
        :isSeparator="true"
      ></TerminalLine>
      <TerminalLine class="component terminal-text-info" :icon="media"
        >manga, light_novels, coding, games</TerminalLine
      >
      <TerminalLine class="component terminal-text-info" :icon="code"
        >html, css, js, c#</TerminalLine
      >
      <TerminalLine class="component terminal-text-info" :icon="anilist"
        ><a href="https://anilist.co/user/cakes/">cakes</a></TerminalLine
      >
      <TerminalLine class="component terminal-text-info" :icon="lastfm"
        ><a href="https://www.last.fm/user/Kex1016">kex1016</a></TerminalLine
      >
      <TerminalLine class="component terminal-text-info" :icon="osu"
        ><a href="https://osu.ppy.sh/users/11328171"
          >cakes on osu</a
        ></TerminalLine
      >
      <TerminalLine class="component terminal-text-info" :icon="steam"
        ><a href="https://steamcommunity.com/id/kex1016">Kex</a></TerminalLine
      >
      <TerminalColors class="colors" />
    </div>
  </div>
</template>

<script>
import TerminalLine from "@/components/Terminal/TerminalLine.vue";
import TerminalColors from "@/components/Terminal/TerminalColors.vue";

// Images for the icons
import logo from "./Images/logo.gif";
import code from "./Images/code.svg";
import media from "./Images/media.svg";
import anilist from "./Images/anilist.png";
import lastfm from "./Images/lastfm.png";
import osu from "./Images/osu.png";
import steam from "./Images/steam.png";

export default {
  name: "TerminalInfo",
  components: {
    TerminalLine,
    TerminalColors,
  },
  data() {
    return {
      logo,
      code,
      media,
      anilist,
      lastfm,
      osu,
      steam,
    };
  },
};
</script>

<style scoped>
.container {
  padding: 10px;
  margin: 50px;
  margin-bottom: 10px;

  display: flex;
  flex-direction: row;
  height: calc(100% - 120px);
  width: calc(100% - 120px);
}

.terminal-image {
  width: 300px;
  height: 300px;
  margin-right: 20px;
}

.terminal-image img {
  width: 100%;
  height: 100%;
}

.component {
  margin: 10px;
}

.terminal-text-title {
  font-size: 25px;
}

.colors {
  margin-top: 20px;
  margin-left: auto;
}
</style>
