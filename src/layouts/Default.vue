<template>
  <div class="layout">
    <Navbar />
    <section class="hero is-medium is-primary">
      <div class="hero-body">
        <div class="container">
          <h1 class="title is-1">
            {{ pageTitle }}
          </h1>
          <h2 v-if="pageSubtitle1" class="subtitle">
            {{ pageSubtitle1 }}
          </h2>
          <h2 v-if="pageSubtitle2" class="subtitle">
            {{ pageSubtitle2 }}
          </h2>
        </div>
      </div>
    </section>
    <main>
      <slot />
    </main>
    <footer class="footer">
      <div class="content has-text-centered">
        <p>Creado por <strong>Diana María Cataño y Yenny Liliana Mosquera</strong>.</p>
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Navbar from '../components/Navbar';
export default {
  props: { pageTitle: '', pageSubtitle1: '', pageSubtitle2: '', color: '' },
  components: { Navbar },
};
</script>

<style lang="scss">
@import '@/assets/scss/overrides.scss';

body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue',
    Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.subtitle {
  margin-bottom: 2px !important;
}

p, li {
  font-size: 25px;
}

img {
  display: flex;
  margin: 10px auto;
}

a {
  font-size: 25px;
  font-weight: 700;
  color: darkblue;
  display: flex;
  justify-content: center;
}

footer {
  padding: 50px 25px !important;
}

iframe, embed {
  border: 3px #140927 solid;
  border-radius: 10px;
  display: flex;
  margin: 50px auto;
  height: 600px;
}

ul li a {
  color: black;
  justify-content: flex-start;
}
</style>
