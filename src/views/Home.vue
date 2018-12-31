<template>
  <div class="home">
    <div class="text-wrapper">
      <div class="line-one">Hello,</div>
      <div class="line-two">I'm Jason</div>
      <br/>
      <div class="line-three">Developer, Creator,</div>
      <div class="line-four">{{selectedSkill}}.</div>
    </div>
    <div @click="handleNav" class="next-chevron"><chevronDoubleDown/></div>

  </div>
</template>

<script>
import chevronDoubleDown from 'vue-material-design-icons/ChevronDoubleDown.vue'
export default {
  name: 'home',
  components: {
    chevronDoubleDown
  },
  created(){
    this.selectedSkill = 'human'
  },
  watch: {
    selectedSkill(){
      let self = this;
      setTimeout(function(){
      let array = self.randomSkill
      self.selectedSkill = array[Math.floor(Math.random() * array.length)];
    }, 2000);
    }
  },
  methods:{
    handleNav(){
      this.$router.push({ path: '/about' })
    }
  },
  data() {
    return {
      randomSkill: ['Friend', 'Gamer', 'Patriots fan', 'Dog lover', 'Environmentalist', 'Fitness enthusiast'],
      selectedSkill: ''
    }
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Playfair+Display|Poppins');
.home{
  height: 100%;
  background-color: #173753;
  color: white;
  display: flex;
  flex-direction: column;
}
.text-wrapper{
  padding-top: 5%;
  display: flex;
  flex-direction: column;
  align-items: baseline;
}
.line-one{
  margin-left: 5%;
  font-size: 5em;
  font-family: 'Poppins', sans-serif;
}
.line-two{
  font-size: 5em;
  margin-left: 5%;
  font-family: 'Poppins', sans-serif;
}
.line-three{
  font-size: 5em;
  margin-left: 15%;
  font-family: 'Playfair Display', serif;
}
.line-four{
  font-size: 5em;
  margin-left: 15%;
  font-family: 'Playfair Display', serif;
  font-style: italic;
}
.next-chevron{
  bottom: 5px;
  align-self: center;
  margin-top: 5%;
  font-size: 4em;
}
</style>
