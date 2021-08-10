<template>
  <div id="app">
    <!-- <img src="./assets/logo.png">
    <HelloWorld/> -->

    <Navbar />
    <router-view></router-view>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Posts from "./components/Posts";
import Contact from "./components/Contact";
import Navbar from "./components/Navbar";

export default {
  name: "App",
  components: {
    HelloWorld,
    Posts,
    Contact,
    Navbar,
  },
};
</script>

<style>
@import "../node_modules/bootstrap/dist/css/bootstrap.min.css";
</style>
