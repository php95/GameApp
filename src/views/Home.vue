<template>
  <div class="home">
    <div
      class="container mb-4"
      style="width: 80%; box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07)"
    >
      <LandingSection />
    </div>
    <Recommended :recommend="recommended"/>
    <Popular :all="games" :filter="filter"/>
  </div>
</template>

<script>
import NavItem from "../components/NavItem";
import Header from "../components/Header";
import Slider from "../components/Slider.vue";
import Search from "../components/Search.vue";
import Button from "../components/Button.vue";
import LandingSection from "../components/LandingSection.vue";
import GameItem from "../components/GameItem.vue";
import Recommended from "../components/Recommended.vue";
import Popular from "../components/Popular.vue";
import Login from "../components/Login.vue";
import axios from "axios";
import Details from "../components/Details.vue";
// @ is an alias to /src

export default {
  name: "Home",
  props:{
    games:Array,
    filter:Array,
    recommended:Array
  },
  

  components: {
    NavItem,
    Header,
    Slider,
    Search,
    Button,
    LandingSection,
    GameItem,
    Recommended,
    Popular,
    Login,
    axios,
    Details,
  },
};
</script>
