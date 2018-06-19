<template>
  <div class="SubLogo">
        <img src="~/assets/img/portfolio.png"/>
  </div>
</template>

<style>
.SubLogo {
  display: inline-block;
  animation: fadein .5s ease-in forwards 2s;
  opacity: 0;
  position: relative;
  overflow: hidden;

}

@keyframes fadein {
  100% {
    opacity: 1;
  }
}
</style>
