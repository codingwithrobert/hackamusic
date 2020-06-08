<template>
  <footer class="footer">
    <p v-html="copyright"></p>
  </footer>
</template>

<script>
export default {
  name: 'footercustom',
  data() {
    return {
      copyright: '&#169; Robert Hernandez 2020 || 2021'
    };
  }
};
</script>

<style scoped>

footer {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #2e004e;
  background-image: linear-gradient(19deg, #2e004e 0%, #b721ff 100%);
  height: 5rem;
  width: 100%;
  position: absolute;
  bottom: 0;
}
p {
  font-family: sans-serif;
  font-size: 0.8rem;
  margin-top: 2rem;
  color: white;
}
</style>