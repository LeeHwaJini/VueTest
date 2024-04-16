<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <CommonHeader />
  <section>
    <BoardTabs />
    <NoticBoardList />
  </section>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import CommonHeader from "./components/CommonHeader.vue";
import BoardTabs from "./components/BoardTabs.vue";
import NoticBoardList from "./components/NoticBoardList.vue";

export default {
  name: "App",
  components: {
    CommonHeader,
    BoardTabs,
    NoticBoardList,
  },
};
</script>

<style>
@import url("~reset-css/reset.css");
#app {
}
section {
  margin: 0 auto;
  max-width: 1200px;
}
</style>
