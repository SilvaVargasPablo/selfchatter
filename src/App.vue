<template>
  <!--nav-->
  <div class="navbar">
    <nav class="navlink">
    <router-link to="/">Home</router-link> |
    <router-link to="/register">register</router-link> |
    <router-link to="/login">login</router-link> |
    <router-link to="/chat">Chat</router-link>
  </nav>
  </div>
  
  <router-view/>
</template>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing:border-box ;
  text-decoration: none;
  list-style-type: none;
  
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: linear-gradient(rgba(5, 0, 12, 0.75),rgba(5, 0, 12, 0.75)), url(./assets/patron.jpg);
}

nav {
  background-color: rgb(241, 108, 13);
  padding: 12px;
  width: 100%;
  height: 60px;
}

nav a {
  font-weight: bold;
  font-size: 1.5em;
  color: #1a2530;
}

nav a.router-link-exact-active {
  color: rgb(16, 177, 32);
  
  margin: 0, 15px;
}

.navlink:hover{
  background-color: rgb(105, 3, 173);
  
}
nav a:hover{
  color: rgb(241, 108, 13)
}
</style>
