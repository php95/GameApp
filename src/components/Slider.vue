<template>
  <div class="Rectangle-Copy">
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
    <NavItem text="sport" :color="color" textColor="white" :mark="mark" />
  </div>
</template>
<script>
import NavItem from "./NavItem.vue";

export default {
  components: { NavItem },
  data() {
    return {
      mark: true,
      color: "gray",
    };
  },
  methods: {
    addTrue() {},
  },
};
</script>
<style scoped>
div {
  display: flex;
}

.Rectangle-Copy {
  margin-top:1%;
  overflow-x: auto;
  overflow-y: hidden;
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: 0px; /* Firefox */
  scrollbar-color: transparent transparent !important;
  width: 102%;
  height: auto;
  margin: -1px -11px 42px;
  padding: 14px 0 16px;
  box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);
  background-color: #ffffff;
}
.Rectangle-Copy::-webkit-scrollbar {
  width: 0px;
  background: transparent transparent !important;
  color: transparent transparent !important;
}
</style>
