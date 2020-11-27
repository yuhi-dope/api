<template>
  <div class="Home">
    <input type="text" v-model="papa" :address="papa"/>
    <button @click="mama">住所自動入力</button>
    <About ></About>
  </div>
</template>

<script>
import About from "./components/About";
export default {
  data() {
    return {
      papa: ""
    };
  },
  components: {
    About
  }
};
</script>
