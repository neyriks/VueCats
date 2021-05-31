<template>
  <div class="cats-wrapper">
    <div class="cats-wrapper-item" v-for="img in image" :key="img.url">
      <img :src="img.url" alt="" />
    </div>
  </div>
  <div class="load-more" @click="getMoreCats">
    <span>Загрузить ещё</span>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "HelloWorld",
  data: () => ({
    image: {
      url: "",
    },
  }),
  created() {
    this.loadNextImage();
  },
  methods: {
    async loadNextImage() {
      try {
        axios.defaults.headers.common["x-api-key"] =
          "41e02190-27d9-4e11-899f-3a2684ed838c";
        let response = await axios.get(
          "https://api.thecatapi.com/v1/images/search",
          { params: { limit: 10, size: "full" } }
        );
        this.image = response.data;
      } catch (err) {
        console.log(err);
      }
    },
    getMoreCats() {
      axios
        .get("https://api.thecatapi.com/v1/images/search", {
          params: { limit: 6, size: "full" },
        })
        .then((response) => {
          // Через конкат дакидывает еще 10 картинок.
          this.image = this.image.concat(response.data);
        });
    },
  },
};
</script>
