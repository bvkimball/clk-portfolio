<template>
  <main>
    <div class="main-content">
      <img class="player1 entrance" src="/img/chris.png"/>
      <span class="menu">
        <h1 class="menu-title">MENU SELECT</h1>
        <span class="menu-row">
          <a href="/gallery/39888311"><img src="~/assets/thumbs/mehat.png" v-on:mouseover="onChangeCharacter('draw', 'Illustrations')"/></a>
          <a href="/gallery/43082852"><img src="~/assets/thumbs/mebeach.png" v-on:mouseover="onChangeCharacter('beach', 'T-Shirt Design')"/></a>
        </span>
        <span class="menu-row">
          <a href="/gallery/46811608"><img src="~/assets/thumbs/meryu.png" v-on:mouseover="onChangeCharacter('ryu', 'Graphic Design')"/></a>
          <img src="~/assets/thumbs/TEMPORARY.png"/>
          <a href="/gallery/39888311"><img src="~/assets/thumbs/mework.png" v-on:mouseover="onChangeCharacter('work', 'Work Stuff')"/></a>
        </span>
        <span class="menu-row">
          <a href="/about"><img src="~/assets/thumbs/mehulk.png" v-on:mouseover="onChangeCharacter('hulk', 'About Me')"/></a>
          <a href="/gallery/39888311"><img src="~/assets/thumbs/meyell.png" v-on:mouseover="onChangeCharacter('negative', 'Unknown')"/></a>
        </span>
      </span>
      <img class="player2 entrance" v-bind:src="'/img/chris_'+ type+ '.png'"/>
      </div>
      <div class="ui ui-1">
        <img src="~/assets/img/box.png"/>
        <img src="~/assets/img/box2.png"/>
      </div>
      <div class="ui ui-2">
        <img src="~/assets/img/1P.png"/>
        <img src="~/assets/img/2P.png"/>
      </div>
      <div class="ui ui-3">
        <div class="gallery-name">Chris L Kimball</div>
        <div class="gallery-name">{{galleryName}}</div>
      </div>
    </main>

</template>
<script>
export default {
  data() {
    return {
      type: "hulk",
      galleryName: "Player 2",
      isActive: false,
      onChangeCharacter(type, name) {
        this.type = type;
        this.galleryName = name;
        this.isActive = true;
      }
    };
  }
};
</script>
<style>
main {
  width: 100%;
}
.main-content {
  display: flex;
  flex-flow: row nowrap;
  align-content: center;
  justify-content: center;
  align-items: center;
  z-index: 1;
}
.ui {
  position: relative;
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-between;
}
.ui-1 {
  margin-top: -50px;
  z-index: 997;
  animation: margins 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) forwards 1.25s;
  opacity: 0;
}
.ui-2 {
  margin-top: -80px;
  padding: 0 20px;
  z-index: 998;
  animation: margins 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) forwards 1.75s;
  opacity: 0;
}
.ui-3 {
  padding: 0 90px;
  z-index: 999;
  animation: margins 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) forwards 2.25s;
  opacity: 0;
}

.menu-title {
  font-family: "Merriweather", serif;
  text-align: center;
  text-transform: uppercase;
  color: #dac751;
  letter-spacing: 0.1em;
  text-shadow: 0px 2px 2px rgba(255, 255, 255, 0.6);
}

.gallery-name {
  font-family: "Merriweather", serif;
  text-align: center;
  text-transform: uppercase;
  color: #dac751;
  letter-spacing: 0.1em;
  text-shadow: 0px 2px 2px rgba(255, 255, 255, 0.6);
}

.menu {
  width: 270px;
  display: inline-block;
  vertical-align: middle;
}
.menu-row {
  display: inline-block;
}
.menu-row img {
  border: 4px solid #fff;
  width: 74px;
  border-radius: 4px;
  margin: 2px;
}
.menu-row img:hover {
  border: 4px solid yellow;
}
.player1 {
  margin-right: -50px;
  width: 350px;
  height: 450px;
  opacity: 0;
}

.player1.entrance {
  animation: slide-left-fade-in 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) forwards 1s;
  transform-origin: center;
}

.player2 {
  width: 350px;
  height: 450px;
  margin-left: -50px;
  align-self: flex-start;
  opacity: 0;
}
.player2.entrance {
  animation: slide-right-fade-in 0.5s cubic-bezier(0.645, 0.045, 0.355, 1) forwards 1s;
  transform-origin: center;
}

@keyframes slide-right-fade-in {
  0% {
    opacity: 0;
    transform: translateX(200px);
  }
  100% {
    opacity: 1;
    transform: translateX(0px);
  }
}

@keyframes slide-left-fade-in {
  0% {
    opacity: 0;
    transform: translateX(-200px);
  }
  100% {
    opacity: 1;
    transform: translateX(0px);
  }
}

@keyframes margins {
  0% {
    margin-left: -500px;
    margin-right: -500px;
    opacity: 0;
  }
  100% {
    margin-left: 0px;
    margin-right: 0px;
    opacity: 1;
  }
}


</style>
