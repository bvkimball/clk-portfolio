<template>
  <main>
    <div class="gallery">
          <masonry class="gallery-content"
            :cols="{default: 4, 1000: 3, 700: 2, 400: 1}"
            :gutter="{default: '5px', 700: '15px', 400: '5px'}"
            >
            <div class="masonry-brick" v-for="(image, index) in images" v-bind:key="index">
                <a v-bind:href="image"><img v-bind:src="image"/></a>
            </div>
          </masonry>
    </div>
  </main>
</template>
<script>

export default {
  props: ['images'],
  mounted() {
    console.log(process.server);
    if(!process.server){
      // const instance = Bricks({
      //   container: '.gallery-content'
      // });
    }
  }
};
</script>
<style>
.gallery {
  max-width: 1150px;
}

.masonry-brick {
  margin: 5px 5px 0px 0px;
}

.masonry-brick img {
  width: 225px;
}
</style>


