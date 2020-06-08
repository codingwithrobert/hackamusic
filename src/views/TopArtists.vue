<template>
  <div>
    <vue-headful title="Top Artists" />
    <div class="search">
      <label for="bySearch">Search your artist</label>
      <input
        v-model="search"
        id="search"
        name="bySearch"
        type="search"
        autofocus
        placeholder="Search..."
      />
    </div>
    <topartiststab :artists="filterArtists" />
    <footercustom />
  </div>
</template>

<script>
// Modulos Requeridos
import api from '@/api/index.js';
import topartiststab from '@/components/TopArtistsTab';
import footercustom from '@/components/FooterCustomTab';

export default {
  name: 'topartists',
  components: { topartiststab, footercustom },
  created() {
    api
      .getArtist()
      .then(response => (this.artists = response.data.topartists.artist));
  },
  data() {
    return {
      artists: [],
      artist: [],
      search: ''
    };
  },
  computed: {
    filterArtists() {
      if (!this.search) {
        return this.artists;
      } else {
        return this.artists.filter(artist =>
          artist.name.toLowerCase().includes(this.search.toLowerCase())
        );
      }
    }
  }
};
</script>
<style scoped>
.search {
  display: flex;
  justify-content: center;
  margin-top: 3rem;
}
label {
  font-size: 1.5rem;
  margin-right: 1rem;
}
input {
  height: 2rem;
  width: 40rem;
}
</style>