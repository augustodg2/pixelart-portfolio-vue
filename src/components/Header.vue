<template>
  <header>
      <section class="title-section">
        <h1>{{title}}</h1>
        <h2>{{subtitle}}</h2>
      </section>

      <a v-bind:href="emailHref">{{email}}</a>
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        title: String,
        subtitle: String,
        email: String,
    },
    computed: {
        emailHref() {
            return `mailto:${this.email}`;
        }
    }
}
</script>

<style scoped>
header {
  margin-bottom: 2.5rem;
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