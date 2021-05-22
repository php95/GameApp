<template>
  <div
    class="container"
    style="
      width: 35%;
      background-color: white;
      box-shadow: 0 2px 10px 0 rgba(0, 0, 0, 0.07);
      padding:3%
     
    "
  >
    <form class="Holder pt-3">
      <div class="form-group">
        <small id="emailHelp" class="form-text text-muted"
          >Please add your account details</small
        ><br />

        
      </div>
      <div class="form-group pt-3" id="input_container ">
        <label for="exampleInputEmail1">Username / Email</label>
        <input
          type="email"
          id="exampleInputEmail1"
          aria-describedby="emailHelp"
          placeholder="Type your username here"
        />
      </div>
      <div class="form-group pt-3" id="input_container ">
        <label for="input">Password</label>
        <input
          type="password"
          id="input"
          placeholder="Type your password here"
        />
        <img
          src="@/assets/hide.png"
          srcset="@/assets/hide@2x.png 2x, @/assets/hide@3x.png 3x"
          class="img-fluid position-absolute mt-2"
          alt="Responsive image"
        />
      </div>
      <div class="login-footer">
        <a href="#" class="-Link mb-3">Forgot password?</a>
        <Button class="mb-4 mt-3" text="Login" />
      </div>
      <div class="text-center  pb-4">
        <a href="#" class="-Link ">Dont have an account? sign up!</a>
      </div>
    </form>
  </div>
</template>
<script>
import Button from "./Button.vue";
export default {
  components: { Button },
};
</script>
<style scoped>
.login-footer {
  text-align: right;
  margin-top: 2%;
}
.Holder {
  text-align: left;
}
small {
    margin-top:3%;

}
label {
  width: 336.6px;
  height: 15px;
  font-family: Roboto;
  font-size: 11px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: left;
  color: #444242;
}
input {
  border: 0px;
  border-bottom: solid 1px #444242;
  padding-bottom: 1%;
}
.-Link {
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
#input_container {
  position: relative;
  background: white;
  width: 100%;
  
}
#input {
  height: auto;
  margin: 0;
  width: 100%;
}
#input_img {
  position: absolute;
}
.img-fluid {
  margin-left: -5%;
}
#exampleInputEmail1{
    height: auto;
  margin: 0;
  width: 100%;

}
</style>
