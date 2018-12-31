<template>
  <div id="app">
    <div id="nav">
      <router-link class="nav-btn nav-home" to="/"> <div>Home</div></router-link>
      <router-link class="nav-btn nav-about" to="/about"><div>About</div></router-link>
      <router-link class="nav-btn nav-work" to="/work"><div>Work</div></router-link>
      <router-link class="nav-btn nav-resume" to="/resume"><div>Resume</div></router-link>
      <router-link class="nav-btn nav-contact" to="/contact"><div>Contact</div></router-link>
    </div>
    <transition name="router-anim" enter-active-class="animated flipInX" leave-active-class="animated flipOutX">
      <router-view></router-view>
    </transition>
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
        // mouseHome: false,
      }
    },
}
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";
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
