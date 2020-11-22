<template>
  <div class="about">
    <div class="weather">
      <h1 class="weather-title">Address:{{ address }}</h1>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  props: ["city"],
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
    this.name = this.data.name;
    this.main = this.data.main;
    this.temp = this.data.main.temp;
    this.humidity = this.data.main.humidity;
    this.speed = this.data.wind.speed;
  }
};
</script>