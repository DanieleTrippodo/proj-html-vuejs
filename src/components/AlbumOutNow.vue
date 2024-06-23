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
      <div>
      <ReadMore> Read More </ReadMore>
      </div>
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
    background-attachment: fixed;
}


/* da usare... */
.blur{
    filter: blur(10px); /* Applica il filtro sfocato */
}
/* da usare... */

.content {
  position: relative;
  z-index: 2;
  padding: 16rem;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.genre {
  color: #f2870c;
  font-size: 1.5em;
  margin: 0;
  font-family: "open-sans", sans-serif;
}
.title {
  font-size: 7em;
  margin-bottom: 3rem;
}
.description {
  font-size: 4.7rem;
  margin-bottom: 1em;
}

ReadMore {
  padding: .9rem 3.5rem;
  background-color: none;
  border: 1px solid #f2870c;
  color: white;
  font-size: 1em;
  cursor: pointer;
  text-transform: uppercase;
  font-weight: 500;
}
</style>