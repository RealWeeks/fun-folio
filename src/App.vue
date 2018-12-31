<template>
  <div id="app">
    <div id="nav">
      <router-link class="nav-btn nav-home" to="/"> <div>Home</div></router-link>
      <router-link class="nav-btn nav-about" to="/about"><div>About</div></router-link>
      <router-link class="nav-btn nav-work" to=""><div>Work</div></router-link>
      <router-link class="nav-btn nav-resume" to=""><div>Resume</div></router-link>
      <router-link class="nav-btn nav-contact" to=""><div>Contact</div></router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
      return {
        mouseHome: false,
      }
    },
}
</script>

<style>
html, body {height: 100%}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
#nav {
  /* padding: 30px; */
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.nav-btn{
  text-decoration: none;
  height: 80px;
  width: 20%;
}
.nav-btn div{
  margin-top: 10%;
  color: white;
  font-size: 3.5em;
}
.nav-home{
  background-color: #173753;
}

.nav-about{
  background-color: #6DAEDB;
}

.nav-work{
  background-color: #2892D7;
}

.nav-resume{
  background-color: #1B4353;
}

.nav-contact{
  background-color: #1D70A2;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

.nav-btn:hover{
  font-size: small;
  align-self: flex-start;
}
</style>
