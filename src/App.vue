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

main{
  width: 100%;
  height: calc((100vh - 80px) - 30px);
  position: relative;
}
</style>
