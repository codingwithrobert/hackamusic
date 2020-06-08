<template>
  <div>
    <vue-headful title="Home" />
    <toptagstab :tags="tags" />

    <footercustom />
  </div>
</template>

<script>
// Modulos y componentes requeridos
import api from '@/api/';
import toptagstab from '@/components/TopTagsTab';
import footercustom from '@/components/FooterCustomTab';

export default {
  name: 'Home',
  components: { toptagstab, footercustom },
  created() {
    api.getTopTags().then(response => (this.tags = response.data.tags.tag));
  },
  data() {
    return {
      tags: [],
      
    };
  }
};
</script>

