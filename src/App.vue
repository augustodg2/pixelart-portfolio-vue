<template>
  <header>
      <section class="title-section">
        <h1>Augusto Dias</h1>
        <h2>Hobbist pixel artist</h2>
      </section>

      <a href="mailto:augustodg2@gmail.com">augustodg2@gmail.com</a>
    </header>
</template>

<script>
export default {
  name: 'App',
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

.title-section {
  margin-bottom: .5rem;
}

h1 {
  font-family: VT323;
  font-size: 6rem;
  font-weight: normal;
  text-shadow: 4px 4px 0 black;
  margin: 0;
}

h2 {
  margin: 0;
  font-size: 2rem;
  font-weight: normal;
}

a {
  text-decoration: none;
  color: white;
}

a:hover {
  text-decoration: underline;
}
</style>
