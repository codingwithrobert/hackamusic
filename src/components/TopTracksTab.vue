<template>
  <div class="container-track">
    <!-- template del componente a exportar  preparado para recibir datos -->
    <div class="toptracks" v-for="track in tracks" :key="track.id">
      <figure>
        <img :src="track.image[2]['#text']" />
      </figure>
      <p>
        <i class="fas fa-music"></i>
        track name: {{ track.name }}
      </p>
      <p>
        <i class="fas fa-users"></i>
        group: {{ track.artist.name }}
      </p>
      <p>
        <i class="fas fa-headphones-alt"></i>
        listeners: {{ track.listeners }}
      </p>
      <p>
        <i class="fas fa-clock"></i>
        time track: {{ track.duration }}
      </p>
      <p>
        <i class="fas fa-paper-plane"></i>
        URL: {{ track.url }}
      </p>
    </div>
  </div>
</template>

<script>
// exportamos componente
export default {
  name: 'toptrackstab',
  props: {
    tracks: Array
  }
};
</script>


<style scoped>
.container-track {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.toptracks {
  display: inline-block;
  padding: 1rem;
  margin: 1rem;
}
figure {
  display: flex;
  justify-content: center;
}

p:last-child {
  padding-bottom: 3rem;
  border-bottom: 0.1rem solid purple;
}
</style>
