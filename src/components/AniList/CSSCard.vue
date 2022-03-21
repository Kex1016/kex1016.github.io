<template>
  <div class="card-container">
    <div
      class="card"
      :style="{ borderColor: `var(--color${borderColor || 1})` }"
      @click="openModal"
      :data-card-name="name"
    >
      <div
        class="card-img"
        :style="{ backgroundImage: `url(${image})` }"
        v-if="image"
      ></div>
      <div class="card-content">
        <div class="card-header">{{ title }}</div>
        <div class="card-body">
          <slot name="card"></slot>
        </div>
      </div>
    </div>
    <CSSModal :name="name" :title="title"><slot name="modal"></slot></CSSModal>
  </div>
</template>

<script>
import CSSModal from "./CSSModal.vue";

export default {
  name: "CSSCard",
  props: {
    title: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: false,
    },
    borderColor: {
      type: Number,
      required: false,
    },
    clickable: {
      type: Boolean,
      required: false,
      default: true,
    },
  },
  components: {
    CSSModal,
  },
  data() {
    return {
      name: this.title.replace(/\s+/g, "-").toLowerCase(),
    };
  },
  methods: {
    openModal() {
      console.log("open: " + this.name);
      document
        .querySelector(`[data-modal-name="${this.name}"]`)
        .classList.add("is-active");
    },
  },
  mounted() {
    let isClickable = this.clickable == "true" || this.clickable == true;
    if (isClickable === false) {
      let el = document.querySelector(`[data-card-name="${this.name}"]`);
      el.classList.add("unclickable");
    }
  },
};
</script>

<style>
.card {
  --width: 360px;
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 10px;
  padding-right: 10px;
  border: 3px solid;
  background-color: var(--background-lighter);
  cursor: pointer;

  /* define max width */
  max-width: var(--width);
  /* define min width */
  min-width: var(--width);

  overflow: hidden;
}

.card.unclickable {
  cursor: default !important;
  pointer-events: none !important;
}

.card .card-img {
  width: 100px;
  height: 100px;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  margin-right: 10px;
}

.card .card-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
}
.card-content .card-header {
  font-size: 1.35rem;
  font-weight: bold;
  margin-bottom: 5px;
}
.card-content .card-body {
  font-size: 1.1rem;
  margin-bottom: 5px;
}
.card-content .card-body *,
.card-content .card-header {
  max-width: calc(var(--width) - 100px - 15px);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
</style>
