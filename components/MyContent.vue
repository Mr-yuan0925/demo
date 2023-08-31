<template>
  <div class="container">
    <div class="card">
      <div class="container-grid">
        <div class="box">
          <img src="https://source.unsplash.com/1000x800">
          <span>CSS</span>
        </div>
        <div class="box">
          <img src="https://source.unsplash.com/1000x802">
          <span>Image</span>
        </div>
        <div class="box">
          <img src="https://source.unsplash.com/1000x804">
          <span>Hover</span>
        </div>
        <div class="box">
          <img src="https://source.unsplash.com/1000x806">
          <span>Effect</span>
        </div>
      </div>
    </div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?1);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?2);"></div>
    <div class="card" style="background-image: url(https://source.unsplash.com/random?3);"></div>
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
  margin: 0px auto;
  padding: 120px 0;
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
.container-grid {
  display: flex;
  width: 100%;
  padding: 4% 2%;
  box-sizing: border-box;
  height: 100%;
}
.box {
  flex: 1;
  overflow: hidden;
  transition: 0.5s;
  margin: 0 2%;
  box-shadow: 0 20px 30px rgba(0, 0, 0, 0.1);
  line-height: 0;
}
.box > img {
  width: 200%;
  height: calc(100% - 10vh);
  object-fit: cover;
  transition: 0.5s;
}
.box > span {
  font-size: 3.8vh;
  display: block;
  text-align: center;
  height: 10vh;
  line-height: 2.6;
}
.box:hover {
  flex: 1 1 50%;
}
.box:hover > img {
  width: 100%;
  height: 100%;
}


</style>
