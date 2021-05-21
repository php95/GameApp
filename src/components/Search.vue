<template>
<div>   
      <div class="form-group col-lg-9" v-show="toggle">
        <input
          type="text"
          class="form-control"
          id="exampleInputPassword1"
          placeholder="Search"
        />
      </div>

        <i
          @click="showInput()"
          class="fas fa-times"
          style="color: red"
          aria-hidden="true"
          v-show="toggle"
        ></i>
        <img
          v-if="!toggle"
          @click="showInput()"
          src="@/assets/Searchicons/Search.png"
          srcset="
            @/assets/Searchicons/Search@2x.png 2x,
            @/assets/Searchicons/Search@3x.png 3x
          "
        />
        <img
          src="@/assets/Searchicons/Dots.png"
          srcset="
            @/assets/Searchicons/Dots@2x.png 2x,
            @/assets/Searchicons/Dots@3x.png 3x
          "
        />
      
</div>
 
</template>
<script>
export default {
  data() {
    return {
      toggle: false,
    };
  },
  props: {},
  methods: {
    showInput() {
      this.toggle = !this.toggle;
    },
  },
};
</script>
<style  scoped>
div {
  display: inline;
}
.form-control {
  width: 30%;
  display: inline;
  margin-right: 10px;
}
.-Icons-Star {
  width: 22px;
  height: 21px;
  margin: 0 5px 0 0;
  object-fit: contain;
}
.-Icons-Dots {
  width: 22px;
  height: 21px;
  margin: 0 0 0 15px;
  object-fit: contain;
}
</style>