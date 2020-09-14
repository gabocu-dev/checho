<template>
  <Layout pageTitle="Teoria Celular" pageSubtitle1="Diana Maria Cataño" pageSubtitle2="Yenny Liliana Mosquera">
    <div class="section">
      <div class="container">
        <p>MAPA MENTAL</p>
        <img src="@/assets/images/mapamental.jpeg" alt="Mapa Mental"/>
        <hr>
        <p>AVATARES</p>
        <br>
        <br>
        <div class="columns">
          <div class="separador">
            <p>DIANA CATAÑO</p>
            <embed type="text/html" src="https://www.voki.com/site/pickup?scid=16788789&chsm=6d34d8000a258736b1da3caab38910e5&allowshare=0" width="1000" height="600">
            <a href="https://www.voki.com/site/pickup?scid=16788789&chsm=6d34d8000a258736b1da3caab38910e5&allowshare=0" target="_blank">Ver en Voki</a>
          </div>
          <div class="separador">
            <p>LILIANA MOSQUERA</p>
            <embed type="text/html" src="https://www.voki.com/site/pickup?scid=16788798&chsm=d4ded44c8feb37e69a4ec7bcbd72c3b6&allowshare=0" width="1000" height="600">
            <a href="https://www.voki.com/site/pickup?scid=16788798&chsm=d4ded44c8feb37e69a4ec7bcbd72c3b6&allowshare=0" target="_blank">Ver en Voki</a>
          </div>
        </div>
      </div>
    </div>
  </Layout>
</template>

<page-query>
  query {
    posts: allPost {
      edges {
        node {
          id
          title
          path
          excerpt
          featuredImage
          author {
            id
            title
            path
            image
          }
          tags {
            id
            path
          }
        }
      }
    }
  }
</page-query>

<script>
export default {
  metaInfo: {
    title: 'La Celula',
  },
};
</script>

<style>
.card {
  margin-bottom: 1.5rem;
}

.cards-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  list-style: none;
  width: 100%;
  justify-content: center;
}

.separador {
  margin: 0 20px;
}

/* Mobile First */
.grid-item {
  width: 100%;
  transition: all 0.2s ease-in-out;
}
/*Medium Width */
@media screen and (min-width: 740px) {
  .grid-item {
    width: calc((100% / 2) - 30px);
  }
}
/*Wide Width */
@media screen and (min-width: 991px) {
  .grid-item {
    width: calc((100% / 3) - 30px);
  }
}
</style>
