<template>
      <Header />
      <Slider />
    <div class="container" style="width:80%">
      <LandingSection />
    </div>
    <!-- <Search/>
  > -->
  <!-- <NavItem text="sport" color="#572589" textColor="white" :mark="false"/>   -->

  <router-view />
</template>
<script>
import NavItem from "./components/NavItem";
import Header from "./components/Header";
import Slider from "./components/Slider.vue";
import Search from "./components/Search.vue";
import Button from "./components/Button.vue";
import LandingSection from "./components/LandingSection.vue";

export default {
  methods: {},
  components: { NavItem, Header, Slider, Search, Button, LandingSection },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
