<template>
  <div class="container">
    <DigitalClock/>
  </div>
</template>

<script>
import DigitalClock from './components/DigitalClock.vue'

export default {
  name: 'App',
  components: {
    DigitalClock
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Covered+By+Your+Grace&display=swap');

body{
font-family:'Covered By Your Grace', cursive; ;
overflow: hidden;
background: conic-gradient(from 90deg at 25% -10%, #ff4500, #d3f340, #7bee85, #afeeee, #7bee85);
}

.container{
width: 95%;
height: 100vh;
margin: auto;
display: flex;
justify-content: center;
align-items: center;
}

</style>
