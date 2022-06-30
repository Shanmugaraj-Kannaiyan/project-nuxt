<template>
  <div>
    <input type="text" v-model="name" />
    <button @click="triggerToast(name, 'success')">Greet</button>
    <button @click="triggerToast(name, 'danger')">Warn</button>
    <Toast ref="toastbar" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
    };
  },
  methods: {
    triggerToast(name, color) {
      if (!this.name) {
        return;
      }
      this.$refs.toastbar.toast(name, color);
    },
  },
};
</script>

<style></style>
