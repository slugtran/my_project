<template>
  <div id="app">
    <div class="container-left">
      <i class="fab fa-accusoft">TO DO LIST</i>
    </div>
    <div class="container-right">
      <router-link class="btnSignIn" to="/signin" type="submit" style="text-decoration : none">Sign In</router-link>
      <router-link class="btnSignUp" to="/signup" type="submit" style="text-decoration : none">Sign Up</router-link>
    </div>
    <!--     <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> -->
  </div>
  <router-view />
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: rgb(221, 233, 241);
  /*  text-align: center;
  color: #2c3e50; */
}

.container-left {
  width: 40%;
  background-color: rgb(216, 221, 219);
  float: left;
  box-sizing: border-box;
  padding: 29.5px;
  text-align: center;
  font-size: 28px;
  color: #e61744;
}
.container-right {
  width: 60%;
  background-color: rgb(216, 221, 219);
  float: right;
  box-sizing: border-box;
  padding: 37px;
  text-align: right;
}

.btnSignIn {
  text-align: center;
  font-size: 18px;
  background: rgb(25, 235, 130);
  margin: 0px 20px 0px 20px;
  padding-left: 4px;
  padding-right: 4px;
}

.btnSignUp {
  font-size: 18px;
}
</style>
