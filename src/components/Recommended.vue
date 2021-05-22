<template>
  <div class="container mb-4" style="width: 80%;box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);">
    <div class="row" style="background-color: white">
      <div class="col-lg-4">
        <h6 class="text-recommend text-left">Most Reccomendation</h6>
      </div>
      <div class="offset-5 col-lg-3">
        <p class="mt-3">
          <a href="#" class="-Link"
            >SEE ALL <i class="fas fa-angle-right"></i
          ></a>
        </p>
      </div>
    </div>
    <div class="row" style="background-color: white;justify-content:space-evenly">
       <div class="col-lg-2" v-for="item in recommend" :key="item.id">
        <GameItem
          :title="item.title"
          :source="item.picture"
          :rate="item.rate"
          :id="item.id"
          class="game-item"
        />
       </div>
    </div>
  </div>
</template>
<script>
import GameItem from "./GameItem.vue";
export default {
  components: { GameItem },
  props:{
    recommend:Array
  }
};
</script>
<style scoped>

.row > * {
  padding: 0;
}
.rating {
  border-radius: 6px;
  background-color: #f2f2f2;
}
.text-recommend {
  padding-top: 5%;
  padding-bottom: 3%;
  text-align:left;
  padding-left:8%
}
.-Link {
  padding-left: 53%;
  font-family: Tajawal;
  font-size: 16px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  text-align: right;
  color: #572589;
  text-decoration: none;
}
.game-item {
  padding-bottom: 20%;
}
</style>
