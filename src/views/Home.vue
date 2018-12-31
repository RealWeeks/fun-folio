<template>
  <div class="home">
    <div class="text-wrapper">
      <div class="line-one">Hello,</div>
      <div class="line-two">I'm Jason</div>
      <br/>
      <div class="line-three">Developer, Enginenner,</div>
      <div class="line-four">{{selectedSkill}}.</div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    // HelloWorld
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
  },
  data() {
    return {
      randomSkill: ['Friend', 'Gamer', 'Patriots fan', 'Dog lover', 'environmentalist'],
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
</style>
