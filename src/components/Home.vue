<template>
  <div class="Header">
    <input type="text" v-model="papa" />
    <button @click="papa">住所自動入力</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      papa: ""
    };
  },
  methods: {
    sendParent() {
      this.$emit("mamapapa", this.papa);
      this.childText = "";
    }
  }
};
</script>
