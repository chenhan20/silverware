<template>
  <div id="app" class="container">
    <div id="nav" class="row">
      <router-link tag="li" class="col-1" to="/">Home</router-link>
      <router-link tag="li" class="col-1" to="/about">About</router-link>
      <router-link tag="li" class="col-1" to="/steve">Steve</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  #nav {
    display: flex;
    justify-content: center;
    li {
      border: solid 1px #35495e;
      list-style: none;
      cursor: pointer;
      &.router-link-exact-active {
        //這個可以判斷他停留的頁面
        background-color: #41b883;
      }
    }
  }
}
</style>