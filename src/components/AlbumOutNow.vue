<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
export default {
  name: 'AlbumOutNow',
  data() {
    return {
      backgroundImage: './src/assets/img/cms_parallax.jpg', // Sostituisci con il percorso dell'immagine di sfondo
      genre: 'INSTRUMENTAL ROCK',
      title: 'ALBUM OUT NOW',
      buttonText: 'READ MORE'
    };
  }
};
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>
  <div class="album-out-now" :style="{ backgroundImage: `url(${backgroundImage})` }">
    <div class="content">
      <h2 class="genre">{{ genre }}</h2>
      <h1 class="title">{{ title }}</h1>
      <ReadMore> Read More </ReadMore>
    </div>
  </div>
</template>



<!-- Qui va lo stile CSS di questo elemento (CSS) -->
<style lang="scss" scoped>
.album-out-now {
    position: relative;
    width: 100%;
    height: 100vh;
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: flex-start;
    text-align: center;
    color: white;
    flex-direction: row;
    align-items: center;
}


/* da usare... */
.blur{
    filter: blur(10px); /* Applica il filtro sfocato */
}
/* da usare... */

.content {
  position: relative;
  z-index: 2;
  padding: 4rem;
}
.genre {
  color: orange;
  font-size: 1.7em;
  margin: 0;
}
.title {
  font-size: 4.7em;
  margin: 0.5em 0;
}
.description {
  font-size: 4.7rem;
  margin-bottom: 1em;
}

ReadMore {
  padding: .9rem 2rem;
  background-color: none;
  border: 1px solid orange;
  color: white;
  font-size: 1.3em;
  cursor: pointer;
}
</style>