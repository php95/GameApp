<template>
  <div class="about">
    <!-- <h1>{{id}} and {{games}}</h1> -->
    <Details :id="id" :game="filterById" />
    <Recommended :recommend="recommended"/>
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

