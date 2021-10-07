<template>
  <transition name="dialog">
    <dialog
      v-if="show"
      open
      class="bg-gray-900 text-gray-50 p-0 border-gray-300 border rounded-xl shadow-lg bg-opacity-75"
      @click="tryClose"
    >
      <section>
        <div class="bg-red-50 p-4 text-red-800 font-bold">
          FOR BOOKING
        </div>
        <div class="p-4">
          <div>
            please contact booking manager Lucka Hájková on following contacts
          </div>
          <br>
          <div>
            Email:  lucka[at]luff.cz
          </div>
          <div>
            Phone: +420 607 669 607
          </div>
        </div>
      </section>
    </dialog>
  </transition>
</template>

<script>
export default {
  name: 'BaseDialog',
  props: {
    show: {
      type: Boolean,
      required: true,
    },
    title: {
      type: String,
      required: false,
      default: '',
    },
    fixed: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
  emits: ['close'],
  methods: {
    tryClose() {
      if (this.fixed) {
        return;
      }
      this.$emit('close');
    },
  },
};
</script>

<style scoped>
.backdrop {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.75);
  z-index: 10;
}
dialog {
  position: fixed;
  top: 20vh;
  left: 10%;
  width: 80%;
  z-index: 100;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  overflow: hidden;
}
@media (min-width: 768px) {
  dialog {
    left: calc(50% - 20rem);
    width: 40rem;
  }
}
</style>
