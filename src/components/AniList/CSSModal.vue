<template>
  <div class="modal" :data-modal-name="name" @openModal="openModal">
    <div class="modal-background" @click="closeModal"></div>
    <div class="modal-card">
      <header class="modal-card-head">
        <p class="modal-card-title">{{ title }}</p>
        <button class="delete" aria-label="close" @click="closeModal"></button>
      </header>
      <section class="modal-card-body">
        <div class="content"><slot></slot></div>
      </section>
      <footer class="modal-card-foot">
        <button class="button is-success" @click="closeModal">Close</button>
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  name: "CSSModal",
  props: {
    name: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
  methods: {
    closeModal() {
      document
        .querySelector(`[data-modal-name="${this.name}"]`)
        .classList.remove("is-active");
    },
  },
};
</script>

<style lang="scss" scoped>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 1000;

  display: none;
  align-items: center;
  justify-content: center;
}

.modal.is-active {
  display: flex;
}

.modal-background {
  background-color: rgba(0, 0, 0, 0.6);

  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
}

.modal-card {
  width: 100%;
  max-width: 600px;
  margin: 0 auto;
  background: var(--color8);
  color: var(--color0);
  padding: 1rem;
  border: 3px solid var(--color0);
}

.modal-card-head {
  display: flex;
  justify-content: space-between;

  padding: 0.5rem;
  padding-left: 0;
  margin-bottom: 1rem;

  border-bottom: 1px solid var(--color0);

  color: var(--color0);
}
.modal-card-head .modal-card-title {
  font-size: 1.5rem;
  font-weight: bold;
  padding: 0;
  margin: 0;
}
.modal-card-head .delete {
  cursor: pointer;

  border: none;
  background: none;
  color: var(--color0);
  font-size: 1.5rem;

  &:hover {
    color: var(--color4);
  }
  &::after {
    content: "×";
  }
}

.modal-card-body {
  padding: 0.5rem;
  padding-left: 0;
  margin-bottom: 1rem;
  text-align: justify;
  font-size: 1.15rem;
}

.modal-card-foot {
  display: flex;
  justify-content: flex-end;

  padding-top: 1rem;
  padding-bottom: 0;
  padding-right: 0;
  margin-top: 1rem;

  border-top: 1px solid var(--color0);
}
.modal-card-foot .button {
  background: var(--color0);
  color: var(--color4);
  border: none;
  font-family: "IBM Plex Mono", monospace;
  font-size: 1.2rem;
  cursor: pointer;

  &:hover {
    background: var(--color4);
    color: var(--color0);
  }
}
</style>
