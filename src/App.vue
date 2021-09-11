<template>
  <Header
    title="Augusto Dias"
    subtitle="Hobbist pixel artist"
    email="augustodg2@gmail.com"
  />
</template>

<script>
import Header from './components/Header';

export default {
  name: 'App',
  components: {
    Header
  },
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  background: #091B49;
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
