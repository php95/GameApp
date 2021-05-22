<template>
  <div class="card" style="width: 100%">
    <img
      :src="userWithIcon.source"
      class="img-fluid card-img-top"
      alt="Responsive image"
    />
    <div class="rating">
      <img
        src="@/assets/Star.png"
        srcset="@/assets/Star@2x.png 2x, @/assets/Star@3x.png 3x"
        class="img-fluid rating-image"
        alt="Responsive image"
      />
      <p class="-Numbers">{{rate}}</p>
    </div>
    <div class="card-body">
      <h1 class="card-text image mt-1" style="height: 42px;">{{title}}</h1>
     <router-link :to="{name:'About',params:{id}}"> <Button text="More Info" /></router-link>
    </div>
  </div>
</template>
<script>
import Button from "./Button.vue";
export default {
  components: { Button },
  props:{
    title:String,
    source:String,
    rate:Number,
    id:Number
  },
  computed: {
  userWithIcon () {
    return {
      source: this.source && require(`@/assets/${this.source}`)
    }
  }
}

};

</script>
<style scoped>
.-Numbers {
  width: 18px;
  height: 16px;
  font-family: Roboto;
  font-size: 12px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: 0.2px;
  text-align: left;
  color: #060606;
  display: inline;
}
.rating-image {
  margin-bottom: 10%;
  margin-right: 14%;
}
.rating {
  width: 48px;
  height: 22px;
  padding: 5px 8px 1px 6px;
  border-radius: 6px;
  background-color: #f2f2f2;
  position: absolute;
  display: flex;
  margin:4%;
}
.card {
  border: 0px;
  padding-right: 4%;
  display:relative;
}
.image {
  font-family: Tajawal;
  font-size: 16.4px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.32;
  letter-spacing: normal;
  text-align: left;
  color: #444242;
}
.card-img-top {
  border-radius: 5px;
  /* position: absolute; */
}
.card-body {
  width: 100%;
  padding: 0px;
  margin: 0px;
  /* position: relative; */
}
</style>
