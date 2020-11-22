<template>
  <div class="Header">
    <input type="text" v-model="childText" />
    <button @click="sendParent">住所自動入力</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      childText: ""
    };
  },
  methods: {
    sendParent() {
      this.$emit("getChildText", this.childText);
      this.childText = "";
    }
  }
};
</script>
