<template>
  <div
    class="container"
    style="
      width: 80%;
      height: 209px;
      box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);
    "
  >
    <div class="row mb-4">
      <img
        :src="userWithIcon.source"
        class="img-fluid card-img-top"
        alt="Responsive image"
        style="height:209px"
      />
    </div>
    <div
      class="row"
      style="
        background-color: white;
        box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);
      "
    >
      <div class="m-3 col-lg-6">
        <p class="headTitle">{{ accessData.title }}</p>
        <p class="subTitle">{{ accessData.description }}</p>
        <p class="downloads">{{ accessData.downloads }} Downloads</p>
       
      </div>
    </div>
    <div class="row"
      style="
        background-color: white;
        box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);"
        >

    </div>
  </div>
</template>
<script>
import Recommended from './Recommended.vue';
export default {
  components: { Recommended },
  name: "Details",
  props: {
    id: Number,
    game: Object,
  },
  data() {
    return {
      game1: {},
    };
  },
  computed: {
    accessData() {
      const data = { ...this.game };
      return data;
    },

    userWithIcon() {
      return {
        source: this.game.picture && require(`@/assets/${this.game.picture}`),
      };
    },
  },

  //   created(){
  //  this.game1 = this.game.find((item) =>
  //         item.id === +this.id
  //       );

  //   },
  //   computed: {
  //     filterById() {
  //       const game1 = this.game.find((item) =>
  //         item.id === +this.id
  //       );
  //       return game1
  //     },
  //     loadData() {
  //      axios.get('http://localhost:8082/'+ this.selectedRoute)
  //               .then(response => (this.chosenRoute = response.data));
  // }

  // },
};
</script>
<style scoped>
.row > * {
  padding: 0;
}
.headTitle {
  width: 100%;
  font-family: Tajawal;
  font-size: 15px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.05;
  letter-spacing: 0.2px;
  text-align: left;
  color: #3c3c3d;
  padding: 6px;
  margin: 1px;
}
.subTitle {
  width: 100%;
  font-family: Tajawal;
  font-size: 14.4px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.32;
  letter-spacing: normal;
  text-align: left;
  color: #444242;
  padding: 6px;
  margin: 1px;
}
.description {
  width: 100%;
  font-family: Tajawal;
  font-size: 17px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.36;
  letter-spacing: normal;
  text-align: left;
  color: #444242;
  padding: 6px;
  margin: 1px;
}
.downloads {
  width: 100%;
  opacity: 0.5;
  font-family: Tajawal;
  font-size: 12px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: 0.22px;
  text-align: left;
  color: #3c3c3d;
  padding: 6px;
  margin: 1px;
}
.DASH-as-fast-as-you {
  width: 100%;

  margin: 5%;
  margin-left: 1%;
  font-family: Tajawal;
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.36;
  letter-spacing: normal;
  text-align: left;
  color: #444242;
}
.DASH-as-fast-as-you .text-style-1 {
  font-family: PingFangSC;
}
.-Link {
  text-align: left;
  font-family: Tajawal;
  font-size: 14px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #572589;
  text-decoration: none;
  margin-right: 85%;
}
</style>