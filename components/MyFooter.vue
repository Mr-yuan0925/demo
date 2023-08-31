<template>
  <div class="Header">
    <div class="Header-love-name">
      <h1>
        <span>l</span>
        <span>x</span>
        <span>y</span>
        <span>❤</span>
        <span>c</span>
        <span>l</span>
        <span>y</span>
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyHeader'
}
</script>

<style scoped>
.Header {
  display: flex;
  border-bottom-left-radius: 30px;
  border-bottom-right-radius: 30px;
  height: 100px;
  position: fixed;
  text-align: center;
  top: 0;
  width: 98%;
  left: 50%;
  transform: translateX(-50%);
  background-color: #FFF;
  z-index: 10;
  flex-direction: row;
  flex-wrap: nowrap;
  align-content: center;
  justify-content: center;
  align-items: center
}

.Header h1 {
  //height: 60px;
}

.Header h1 span {
  position: relative;
  top: 0px;
  display: inline-block;
  animation: bounce .3s ease infinite alternate;
  font-family: fantasy;
  font-size: 80px;
  color: #f1677b;
  text-shadow: 0 1px 0 #dca3ad,
  0 2px 0 #dca3ad,
  0 3px 0 #dca3ad,
  0 4px 0 #dca3ad,
  0 5px 0 #dca3ad,
  0 6px 0 transparent,
  0 7px 0 transparent,
  0 8px 0 transparent,
  0 9px 0 transparent,
  0 10px 10px rgba(209, 52, 52, .4);
}

.Header h1 span:nth-child(2) { animation-delay: .1s; }
.Header h1 span:nth-child(3) { animation-delay: .2s; }
.Header h1 span:nth-child(4) { animation-delay: .3s; color: #e11c3a;
}
.Header h1 span:nth-child(5) { animation-delay: .4s; }
.Header h1 span:nth-child(6) { animation-delay: .5s; }
.Header h1 span:nth-child(7) { animation-delay: .6s; }
.Header h1 span:nth-child(8) { animation-delay: .7s; }

@keyframes bounce {
  100% {
    top: -10px;
    text-shadow: 0 1px 0 #dca3ad,
    0 2px 0 #dca3ad,
    0 3px 0 #dca3ad,
    0 4px 0 #dca3ad,
    0 5px 0 #dca3ad,
    0 6px 0 #dca3ad,
    0 7px 0 #dca3ad,
    0 8px 0 #dca3ad,
    0 9px 0 #dca3ad,
    0 50px 25px rgba(209, 52, 52, .2);
  }
}
</style>

