<template>
  <div id="app">
    <Header />
    <main>
      <DiscsList />
    </main>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import DiscsList from "./components/DiscsList.vue";

export default {
  name: "App",
  components: {
    Header,
    DiscsList,
  },
};
</script>

<style lang="scss">
@import "./style/general";
</style>
