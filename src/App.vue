<template>
  <div id="app">
    <Header @getChildText="showChildText"></Header>
    <p v-for="(item,index) in textList" :key="index" :city="data.city">Address:{{item}}</p>
  </div>
</template>

<script>
import About from "./components/About";
import Home from "./components/Home";
export default {
  data() {
    return {
      childText: "",
      item: ""
    };
  },
  methods: {
    showChildText(childText) {
      this.textList.push(childText);
    }
  },
  components: {
    About,
    Home
  }
};
</script>