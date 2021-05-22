<template>
  <div class="row" style="background-color:white;box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);display:relative">
    <div class="offset-1 col-lg-3 col-md-10">
      <Logo />
    </div>
    <div class="offset-2 col-lg-4 mt-4 col-md-6 col-sm-8 col-8 pt-3">
      <div class="form-group" v-show="toggle">
        <input
          type="text"
          class="form-control"
          id="exampleInputPassword1"
          placeholder="Search"
        />
      </div>
    </div>
    <div class="col-lg-1 col-md-2 mt-4 col-sm-2 col-2 pt-3">
      <i
        @click="showInput()"
        class="fas fa-times"
        style="color: red"
        aria-hidden="true"
        v-show="toggle"
      ></i>
      <img
        class="-Icons-Dots img-fluid"
        v-if="!toggle"
        @click="showInput()"
        src="@/assets/Searchicons/Search.png"
        srcset="
          @/assets/Searchicons/Search@2x.png 2x,
          @/assets/Searchicons/Search@3x.png 3x
        "
      />
      <img
        class="-Icons-Dots img-fluid"
        src="@/assets/Searchicons/Dots.png"
        srcset="
          @/assets/Searchicons/Dots@2x.png 2x,
          @/assets/Searchicons/Dots@3x.png 3x
        "
        @click="showLogin()"
      />
      
    </div>
  </div>
    <Login style="
    border-radius: 5px;
    position: absolute;
    margin-top:-2%;
    width: 35%;
    background-color: white;
    box-shadow: rgb(0 0 0 / 7%) 0px 2px 10px 0px;
    margin-left: 55%;
    z-index: 1;"
    v-show="logForm"/>
</template>


<script>
import Login from './Login.vue';
import Logo from "./Logo.vue";
import Search from "./Search.vue";
import axios from 'axios';
export default {
  components: { Search, Logo,Login,axios},
  
    data() {
    return {
      toggle: false,
      logForm: false
    };
  },
  methods: {
    showInput() {
      this.toggle = !this.toggle;
    },
    showLogin() {
      this.logForm = !this.logForm;
    },
  },
};
</script>
<style scoped>
.container {
  margin: 0px;
  padding: 0px;
}
.-Background {
  display: flex;
  width: 1366px;
  height: 100px;
  padding: 20px 200px 13px 0;
  box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);
}
.form-control {
  width: 100%;
  display: inline;
  margin-right: 10px;
}

.-Icons-Dots {
  width: 25%;
  /* height: 21px;
  margin: 0 0 0 15px; */
  object-fit: contain;
}
</style>