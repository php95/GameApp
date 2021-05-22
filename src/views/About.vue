<template>
  <div class="about">
    <!-- <h1>{{id}} and {{games}}</h1> -->
    <div class="row">
    <Details :id="id" :game="filterById" />
    </div>
    <div class="row">
    <Recommended :recommend="recommended" style="margin-top:18%"/>
    </div>
  </div>
</template>
<script>
import Details from "../components/Details"
import Recommended from "../components/Recommended"
export default {
  name:"About",
  props:{id:Number,games:Array, recommended:Array},
  components:{
    Details,Recommended
  },
   computed: {
    filterById() {
      const game1 = this.games.find((item) => 
        item.id === +this.id 
      );
      return game1
    }
    }
}
</script>

