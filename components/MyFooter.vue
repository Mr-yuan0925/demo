<template>
  <div class="Footer">
    <div id="clock">
      <p class="date">{{ date }}</p>
      <p class="time">{{ time }}</p>
      <p class="text">DIGITAL CLOCK with Vue.js</p>
    </div>
  </div>
</template>

<script>
const week = ['SUN', 'MON', 'TUE', 'WED', 'THU', 'FRI', 'SAT'];
export default {
  name: 'MyHeader',
  data() {
    return {
      date: '',
      time: '',
      timer: null
    }
  },
  mounted() {
    this.timer = setInterval(()=>{
      this.updateTime();
    },1000)
  },
  beforeDestroy() {
    if(this.timer){
      clearInterval(this.timer);
    }
  },
  methods: {
    updateTime() {
      const cd = new Date();
      this.time = this.zeroPadding(cd.getHours(), 2) + ':' + this.zeroPadding(cd.getMinutes(), 2) + ':' + this.zeroPadding(cd.getSeconds(), 2);
      this.date = this.zeroPadding(cd.getFullYear(), 4) + '-' + this.zeroPadding(cd.getMonth()+1, 2) + '-' + this.zeroPadding(cd.getDate(), 2) + ' ' + week[cd.getDay()];
    },
    zeroPadding(num, digit) {
      let zero = '';
      for(let i = 0; i < digit; i++) {
        zero += '0';
      }
      return (zero + num).slice(-digit);
    }
  },

}
</script>

<style scoped>
.Footer {
  display: flex;
  border-top-left-radius: 30px;
  border-top-right-radius: 30px;
  height: 150px;
  position: fixed;
  text-align: center;
  bottom: 0;
  width: 98%;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
  flex-direction: row;
  flex-wrap: nowrap;
  align-content: center;
  justify-content: center;
  align-items: center;
  background: #0f3854;
  background: radial-gradient(ellipse at center,  #0a2e38  0%, #000000 70%);
  background-size: 100%;
}
#clock {
  font-family: "Share Tech Mono", monospace;
  color: #ffffff;
  text-align: center;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  color: #daf6ff;
  text-shadow: 0 0 20px #0aafe6, 0 0 20px rgba(10, 175, 230, 0);
}
#clock .time {
  letter-spacing: 0.05em;
  font-size: 50px;
}
#clock .date {
  letter-spacing: 0.1em;
  font-size: 18px;
}
#clock .text {
  letter-spacing: 0.1em;
  font-size: 12px;
  padding: 10px 0 0;
}

</style>

