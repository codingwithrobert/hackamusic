<template>
  <div class="about">
    <vue-headful title="About" />
    <h2>This Website was created by Robert Hernandez</h2>
    <figure>
      <img :src="urlImage" alt="Eddy Murphy" />
    </figure>

    <a href="https://instagram.com/dimelorobert">
      <i class="fab fa-instagram"></i>
    </a>
    <p></p>
    <p>Resources that I used to create this website</p>
    <p>
      <a href="https://www.last.fm/api/?lang=es&">API Last FM</a>
    </p>
    <p>
      <a href="https://www.npmjs.com/package/axios">Axios</a>
    </p>
    <p>
      <a href="https://www.npmjs.com/package/vue-headful">Vue-Headful</a>
    </p>
    <footercustom></footercustom>
  </div>
</template>

<script>
import footercustom from '@/components/FooterCustomTab';

export default {
  name: 'About',
  components: { footercustom },
  data() {
    return {
      urlImage: 'https://bit.ly/3cGIaLK'
    };
  }
};
</script>

<style scoped>
.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
h2 {
  color: rgb(58, 14, 100);
  font-size: 3rem;
}
figure {
  display: flex;
  justify-content: center;
}
figure img {
  width: 20rem;
  border-radius: 50%;
}
.fa-instagram {
  font-size: 4rem;
}
</style>