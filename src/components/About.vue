<template>
  <div class="About">
    <h1 class="add" :ress="come" >Address:{{ address }}</h1>
  </div>
</template>

<script>
import axios from "axios";
export default {
  props: ["address"],
  data() {
    return {
      address:"",
    };
  },
  async created() {
    let item = await axios.get(
      `https://apis.postcode-jp.com/api/v3/postcodes?postcode=279-0031
`
    );
    this.data = item.data;
    this.address = this.data.address;
  },
  methods: {
    mama() {
      this.$emit(this.papa,"add");
      this.papa = "";
    }
  },
};
</script>