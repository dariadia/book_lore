<template>
  <div class="VueToNuxtLogo">
    <div class="Triangle Triangle--two2" />
    <div class="Triangle Triangle--one1" />
    <div class="Triangle Triangle--three3" />
    <div class="Triangle Triangle--four" />
  </div>
</template>

<style>
.VueToNuxtLogo {
  display: inline-block;
  animation: turn 2s linear forwards 1s;
  transform: rotateX(180deg);
  position: relative;
  overflow: hidden;
  height: 80px;
  width: 145px;
}

.Triangle {
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 0;
}

.Triangle--one1 {
  border-left: 105px solid transparent;
  border-right: 105px solid transparent;
  border-bottom: 180px solid #2016a7;
}

.Triangle--two2 {
  top: 30px;
  left: 35px;
  animation: goright 0.5s linear forwards 3.5s;
  border-left: 87.5px solid transparent;
  border-right: 87.5px solid transparent;
  border-bottom: 150px solid #28aed6;
}

.Triangle--three3 {
  top: 60px;
  left: 35px;
  animation: goright 0.5s linear forwards 3.5s;
  border-left: 70px solid transparent;
  border-right: 70px solid transparent;
  border-bottom: 120px solid #3b065c;
}

.Triangle--four {
  top: 120px;
  left: 70px;
  animation: godown 0.5s linear forwards 3s;
  border-left: 35px solid transparent;
  border-right: 35px solid transparent;
  border-bottom: 60px solid #fff;
}

@keyframes turn {
  100% {
    transform: rotateX(0deg);
  }
}

@keyframes godown {
  100% {
    top: 180px;
  }
}

@keyframes goright {
  100% {
    left: 70px;
  }
}
</style>
