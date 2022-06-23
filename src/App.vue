<template>
  <nav>
    <div class="menu"><router-link to="/">후보등록</router-link></div>
    <div class="menu"><router-link to="/voting">투표</router-link></div>
    <div class="menu"><router-link to="/result">개표결과</router-link></div>
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  border: 5px solid blue;
  border-spacing: 1%;
  width: 80%;
  margin-top: 5%;
  margin-left: auto;
  margin-right: auto;
  padding-bottom: 3%;
  background-color: white;
}

nav {
  padding: 30px;
  text-decoration-line: none;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration-line: none;
}

nav a.router-link-exact-active {
  color: #42b983;
  text-decoration-line: none;
}

a:link {
  color: black;
}
a:visited {
  color: black;
}

body{
  background-size: 100% auto;
  background-image: url('@/assets/bgimage_election.png');
  background-repeat: no-repeat;
  background-position: center top;
}
.menu{
  display: inline-block;
  border:3px black solid;
  width:20%;
  margin: 1%;
  text-align: center;
  font-size: 30px;
  box-shadow: 2px 2px 4px 2px #dadce0;
}
</style>
