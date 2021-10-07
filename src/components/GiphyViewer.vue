<template>
  <div>
    <b-card-group columns>
      <b-card
        v-for="gif in gifs"
        :key="gif"
        :img-src="gif.images.fixed_width.url"
        :img-alt="gif.title"
      >
        <b-card-text>
          <a :href="gif.url" target="_blank"> {{ gifs[0].title }} </a>
        </b-card-text>
      </b-card>
    </b-card-group>
  </div>
</template>

<script>
import axios from "axios";
const API_KEY = "KZq2hE4TiuLAlG0r3SONT5xGXeMWqaud";
const GIPHY_URL = "https://api.giphy.com/v1/gifs";
export default {
  name: "GiphyViewer",

  data() {
    return {
      gifs: [],
    };
  },
  mounted() {
    axios
      .get(`${GIPHY_URL}/trending?api_key=${API_KEY}`)
      .then((response) => {
        console.log(response.data.data);
        this.gifs = response.data.data;
      })
      .catch((error) => console.log(error));
  },
  methods: {},
};
</script>

<style>
</style>