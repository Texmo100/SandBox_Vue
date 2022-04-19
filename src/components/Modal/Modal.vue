<template>
  <transition name="modal-fade">
    <div class="backdrop">
      <div class="modal">
        <button
          type="button"
          class="btn-close--corner"
          @click="close"
          aria-label="Close modal"
        >
          x
        </button>

        <header class="modal__header">
          <h1>Modal Header</h1>
        </header>
        <div class="modal__body">Modal Body</div>
        <footer class="modal__footer">
          <button type="button" class="btn-close--main" @click="close">Close modal</button>
        </footer>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Modal",
  methods: {
    close() {
      this.$emit("close");
    },
  },
};
</script>

<style scoped>
.backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  width: 40rem;
  height: 40rem;
  position: relative;
  background: #ffffff;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  border-radius: 1rem;
  z-index: 3;
}

.btn-close--corner {
  position: absolute;
  top: 0;
  right: 0;
  border: none;
  background-color: transparent;
  border-radius: 0.5rem;
  padding: 2rem;
  color: #e30b5c;
  transition: all 300ms ease;
}

.btn-close--corner:hover {
  cursor: pointer;
  background-color: #e5e5e5;
  border-top-right-radius: 1rem;
}

.modal__header,
.modal__body,
.modal__footer {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.btn-close--main {
  border: none;
  width: 100%;
  height: 4rem;
  background-color: #e1e1e1;
  border-radius: 0.5rem;
  transition: all 300ms ease;
}

.btn-close--main:hover {
  cursor: pointer;
  color: #e8e8e8;
  background-color: #e30b5c;
}

.modal-fade-enter,
.modal-fade-leave-to {
  opacity: 0;
}

.modal-fade-enter-active,
.modal-fade-leave-active {
  transition: opacity 0.5s ease;
}
</style>