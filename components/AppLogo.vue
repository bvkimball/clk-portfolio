<template>
  <div class="MainLogo">
        <img src="~/assets/img/logo.png"/>
  </div>
</template>

<style>
.MainLogo {
  display: inline-block;
  animation: down .5s ease-in forwards 0s;
  transform: translateY(-180px);
  position: relative;
  overflow: hidden;

}

@keyframes down {
  100% {
    transform: translateY(0px);
  }
}
</style>
