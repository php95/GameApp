<template>

  <div class="item Rectangle Games" :style="{ background: color,color:textColor }">
     {{ text }}
    <img src="@/assets/Tick.png" alt="" class="icons-tick " v-if="mark"/>
  </div>
 
</template>
<script>
export default {
  props: {
    text: String,
    color: String,
    mark: Boolean,
    textColor:String
  },
  
};
</script>
<style scoped>
.item{
    display: flex;
}
.Rectangle {
  width: 70px;
  height: 30px;
  margin: 0 8px;
  padding: 5px 14px 5px 16px;
  border-radius: 12.5px;
  border: solid 1px #d2d2d2;
  background-color: #d8d8d8;
}
.Games {
  
  font-family: Tajawal;
  font-size: 14.4px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
  color: #545454;
}
.icons-tick {
  width: 11px;
  height: 8.7px;
  margin: 6.4px 0 4.9px 5px;
  object-fit: contain;
}
</style>