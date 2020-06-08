<template>
  <div>
    <vue-headful title="ERROR" />
    <h1>ERROR</h1>
    <h2>404</h2>
    <p>Where are you going, my frined?</p>
    <footercustom></footercustom>
  </div>
</template>

<script>
import footercustom from '@/components/FooterCustomTab';

export default {
  name: 'Error',
  components: { footercustom }
};
</script>

<style scoped>
h2 {
  font-size: 3rem;
}

p {
  font-size: 2rem;
}
</style>