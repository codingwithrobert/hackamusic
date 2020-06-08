<template>
  <div>
    <vue-headful title="Top Tracks" />
    <toptrackstab :tracks="tracks" />

    <footercustom />
  </div>
</template>

<script>
// Modulos Requeridos
import api from '@/api/index.js';
import toptrackstab from '@/components/TopTracksTab';
import footercustom from '@/components/FooterCustomTab';

export default {
  name: 'toptracks',
  components: { toptrackstab, footercustom },
  created() {
    api
      .getTopTracks()
      .then(response => (this.tracks = response.data.tracks.track));
  },
  data() {
    return {
      tracks: []
    };
  }
};
</script>