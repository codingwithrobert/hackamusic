<template>
  <div class="container-artist">
    <!-- template del componente a exportar  preparado para recibir datos-->
    <div class="topartists" v-for="artist in artists" :key="artist.id">
      <figure>
        <img :src="artist.image[2]['#text']" />
      </figure>
      <p>
        <i class="fas fa-microphone-alt"></i>
        Artist:
        {{ artist.name }}
      </p>
      <p>
        <i class="fas fa-headphones-alt"></i>
        Listeners: {{ artist.listeners }}
      </p>
      <p>
        <i class="fas fa-paper-plane"></i>
        Url: {{ artist.url }}
      </p>
    </div>
  </div>
</template>

<script>
// exportamos componente
export default {
  name: 'topartiststab',
  props: {
    artists: Array
  }
};
</script>


<style scoped>
.container-artist {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.topartists {
  display: inline-block;
  padding: 1rem;
  margin: 1rem;
}
figure {
  display: flex;
  justify-content: center;
}
p {
  text-align: center;
}
p:last-child {
  padding-bottom: 3rem;
  border-bottom: 0.1rem solid purple;
}
</style>