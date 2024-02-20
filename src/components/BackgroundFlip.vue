<template>
  <div class="background">
    Background-color: <span :style="{color: change}">{{ change }}</span>
  </div>
  <button class="button" @click="novaCor">Click</button>
</template>

<script>

export default {
  name: 'BackgroundFlip',
  props: {},
  emits: ['clicou'],
  data() {
    return {
      change: "rgb(146, 166, 255)"
    }
  },
  methods:{
    novaCor(){
     
      const randomColor = '#' + Math.floor(Math.random()*16777215).toString(16);
      
      this.change = randomColor;

      this.$emit('clicou', randomColor)

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background{
  color: white;
  font-weight: 500;
  border-radius: 5px;
  padding: 1.5rem;
  background-color: rgb(0, 0, 0, .5);
  margin-top: 15%;
}

.button{
  border-radius: 5px;
  color: #333;
  margin-top: 5%;
  padding: .8rem;
  font-weight: 500;
  border: none;
  background-color: #fff;
  transition: .3s ease-in-out;
}

.button:hover{
  cursor: pointer;
  transform: scale(1.05);
}
.button:focus{
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.5);
}
</style>
