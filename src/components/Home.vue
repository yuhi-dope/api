<template>
  <div class="Header">
    <input type="text" v-model="papa" :city="papa"/>
    <button @click="mama">住所自動入力</button>
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
    mama() {
      this.$emit(this.papa,"add");
      this.papa = "";
    }
  }
};
</script>
