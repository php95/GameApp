<template>
      <Header />
      <Slider style="position:relative" />
    <div class="container mb-4" style="width:80%;box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07); ">
      <LandingSection />
    </div>
  
      <Recommended />
      <Popular/>
      

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
import GameItem from "./components/GameItem.vue"
import Recommended from './components/Recommended.vue';
import Popular from './components/Popular.vue';
import Login from './components/Login.vue';


export default {
  methods: {},
  components: { NavItem, Header, Slider, Search, Button, LandingSection,GameItem, Recommended, Popular, Login},
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
