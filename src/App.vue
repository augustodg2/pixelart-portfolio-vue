<template>
  <Header
    title="Augusto Dias"
    subtitle="Hobbist pixel artist"
    email="augustodg2@gmail.com"
  />
  <Gallery :images="images" />
</template>

<script>
import Header from './components/Header.vue';
import Gallery from './components/Gallery.vue';
import images from './data/image-list.json';

export default {
  name: 'App',
  components: {
    Header,
    Gallery,
  },
  data() {
    return {
      images
    }
  },
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  background: #345dc5;
  color: #FFF;
  font-family: 'Open Sans';
}

#app {
  max-width: 700px;
  width: 100%;
  margin: auto;
  text-align: center;
  padding-top: 2rem;
}
</style>
