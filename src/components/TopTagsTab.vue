<template>
  <div class="container-tags">
    <!-- template del componente a exportar  preparado para recibir datos -->
    <div class="toptags" v-for="tag in tags" :key="tag.id">
      <p>
        <i class="fas fa-music"></i>
        Genre: {{ tag.name }}
      </p>
      <p>
        <i class="fas fa-users"></i>
        {{ tag.reach }} || followers
      </p>

      <p>
        <i class="fas fa-tags"></i>
        {{ tag.taggings }} || tagged
      </p>
      <p class="url">
        <i class="fas fa-paper-plane"></i>
        URL: {{ tag.url }}
      </p>
    </div>
  </div>
</template>

<script>
/* exportamos componente*/
export default {
  name: 'toptagstab',
  props: {
    tags: Array
  }
};
</script>


<style scoped>
.container-tags {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.toptags {
  display: inline-block;
  padding: 1rem;
  margin: 1rem;
  text-align: left;
}
p:last-child {
  padding-bottom: 3rem;
  border-bottom: 0.1rem solid purple;
}
</style>