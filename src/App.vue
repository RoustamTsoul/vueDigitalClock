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
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Symbols+2&display=swap');

body{
font-family:'Noto Sans Symbols 2', sans-serif;
overflow: hidden;
background: conic-gradient(from 90deg at 25% -10%, #a6583b, #d3f340, #5a945f, #a9f9f9, #50cb5a);
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
