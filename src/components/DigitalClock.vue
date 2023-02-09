<template>
  <div class="digital-clock">
    <h1 class="day">{{day}}</h1>
    <h1 class="hour">{{ hours }}</h1>
    <h1 class="bar">:</h1>
    <h1 class="minute">{{minutes}}</h1>
    <h1 class="ampm">{{ampm}}</h1>             
  </div>
</template>

<script>
export default {
    data(){
        return{
            day:'',
            dayNumber:'',
            hours:'',
            minutes:'',
            ampm:'',
            dayNames:[],  
        }
    },

     mounted() {
        setInterval(() => this.calculateTime(), 1000)
        // setTimeout(this.calculateTime(), 200);
    },

    methods:{
        calculateTime(){
            const date = new Date();
            const dayNumber = date.getDay();
            const hours = date.getHours();
            const minutes = date.getMinutes();
            const ampm = hours >= 12 ? 'P.M.' : 'A.M.';
            const dayNames = ["SUN","MON","TUE","WED","THU","FRI","SAT"]
            const day = dayNames[dayNumber];
            
            this.hours = hours % 12;
            this.hours = hours ? hours: '12';
            this.hours = hours < 10 ? '0' + hours : hours;
            this.minutes = minutes < 10 ? '0' + minutes : minutes;


            this.hours = hours;
            this.minutes = minutes;
            this.ampm = ampm;
            this.dayNumber = dayNumber;
            this.date = date;
            this.dayNames = dayNames;
            this.day = day;

            
        }
    },

    
}
</script>

<style scoped>
.digital-clock{
 width: fit-content;
 margin: auto;
 padding: 20px;
 border-radius: 5px;
 color:rgb(223, 16, 16);
 background-color: #ff440046;
}

.digital-clock h1{
display: inline-block;
margin:0 10px;
font-weight: bold;
font-size: 5rem;
}
</style>