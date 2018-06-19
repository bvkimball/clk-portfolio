<template>
  <section class="container">
    <app-logo/>
    <app-gallery v-bind:images="images"/>
  </section>
</template>

<script>
import axios from "axios";
import Vue from "vue";
import VueMasonry from 'vue-masonry-css'
import AppLogo from '~/components/AppLogo.vue'
import AppGallery from '~/components/AppGallery.vue'

Vue.use(VueMasonry);

export default {
  components: {
    AppLogo,
    AppGallery
  },
  async asyncData({params}) {
        console.log(params);

    let deviations = [];
    let sources = [];
    let url = `http://backend.deviantart.com/rss.xml?q=gallery:patmos/${params.id}`;
    let yql =
      "http://query.yahooapis.com/v1/public/yql?q=" +
      escape('select * from xml where url="' + url + '"') +
      "&_maxage=86400&format=json";

    let raw = await axios.get(yql);
    let feed = raw.data;
    console.log(feed);
    let items = feed.query.results.rss.channel.item;

    for (let i = 0, l = items.length; i < l; i++) {
      let object = {};
      object.title = items[i].title[0];
      object.image = items[i].content.url;
      deviations.push(object);
      sources.push(items[i].content.url);
    }
    console.log(sources);

    return {
      images: sources
    };
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Merriweather:400,700');
@import "~/assets/less/app.less";

.container {
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
