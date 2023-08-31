<template>
  <div class="container">
    <div class="card" style="background-image: url(https://source.unsplash.com/random?1);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?2);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?3);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?4);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?5);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?6);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?7);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?8);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?9);"></div>
  </div>
</template>

<style scoped>
.container {
  align-content: flex-start;
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: space-around;
  width: 80vw;
}
.container .card {
  aspect-ratio: 16 / 9;
  background: white;
  background-position: center;
  background-size: cover;
  border-radius: 20px;
  flex-shrink: 0;
  margin-bottom: 10%;
  width: 100%;
}
</style>
