<template>
  <div class="css">
    <CSSCard title="Zenbu-ish" image="/img/css/zenbu.png" :borderColor="1">
      <template v-slot:card>
        <div>An edit of Sigma's CSS</div>
      </template>
      <template v-slot:modal>
        <div>
          This is the first CSS I've "written" with compatibility in mind. It
          should work with any version of AniList, as long as they don't change
          or add the fundamentals. The original version was written by
          <a href="https://anilist.co/user/Sigma">Sigma</a>. The original has
          been updated quite a lot since then, but this is the last version I
          had on hand.
        </div>
        <div class="preview">
          <img
            src="https://files.nyilcomp.hu/QeNe3/jEfENuju63.png/raw"
            alt="Zenbu-ish"
          />
        </div>
        <div>
          <a href="https://downloads.nyilcomp.hu/css/anilist/zenbuish.css"
            >Download (or link for @import)</a
          >
        </div>
      </template>
    </CSSCard>
    <CSSCard title="Mango" image="/img/css/mango.png" :borderColor="3">
      <template v-slot:card>
        <div>Pretty hecking modular.</div>
      </template>
      <template v-slot:modal>
        <div>
          I consider this my best work so far. Most of the things a regular user
          would want to change, like the colors or if the elements are
          "cartoon-y" or not are actually changeable. And I mean the colors are
          *really* easy to change.
        </div>
        <div class="preview">
          <img
            src="https://files.nyilcomp.hu/QeNe3/NaXeJEHi86.png/raw"
            alt="Mango"
          />
        </div>
        <div>
          <a href="https://downloads.nyilcomp.hu/css/anilist/mango.css"
            >Download (or link for @import)</a
          >
        </div>
      </template>
    </CSSCard>
    <CSSCard
      title="More soon?"
      :clickable="false"
      image="/img/css/moresoon.png"
      :borderColor="15"
    >
      <template v-slot:card>
        <div>Maybe...</div>
      </template>
    </CSSCard>
  </div>
</template>

<script>
import CSSCard from "./CSSCard.vue";

export default {
  name: "CSSList",
  components: {
    CSSCard,
  },
};
</script>

<style scoped>
.css {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 10px;
  margin-bottom: 15px;
}

.css a {
  color: var(--color9);
}

.css > div {
  margin-left: 5px;
  margin-right: 5px;
}

.css .preview img {
  width: 100%;
  margin-top: 10px;
  margin-bottom: 10px;
}
</style>
