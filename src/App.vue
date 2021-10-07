<template>
  <b-container id="app">
    <b-row>
      <b-col>
        <GiphyViewer />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import GiphyViewer from "@/components/GiphyViewer.vue";

export default {
  name: "App",
  components: {
    GiphyViewer,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
      