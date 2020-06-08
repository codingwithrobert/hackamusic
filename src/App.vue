<template>
  <div id="app">
    <figure class="logo">
      <a :href="home">
        <img src="./assets/images/logo.png" alt="logo" />
      </a>
    </figure>
    <!-- Enlaces reactivos para que sea mas facil su mantenimiento  -->
    <div id="nav">
      <ul>
        <li>
          <a :href="home">
            <h1 :href="home">HACKAMUSIC</h1>
          </a>
        </li>
        <li>
          <router-link :to="{ name:'Home'}">Home</router-link>
        </li>
        <li>
          <router-link :to="{ name:'TopArtists'}">Artists</router-link>
        </li>
        <li>
          <router-link :to="{ name:'TopTracks'}">Songs</router-link>
        </li>
        <li>
          <router-link :to="{ name:'About'}">About</router-link>
        </li>
      </ul>
      <!-- Enlaces reactivos para que sea mas facil su mantenimiento  -->
    </div>
    <router-view />
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: 'Top best music genres',
      home: '/'
    };
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;1,100&display=swap');
html {
  position: relative;
}
#app {
  font-family: 'Roboto', sans-serif;
}

.logo {
  display: flex;
  justify-content: center;
  align-items: center;
}
.logo img {
  width: 30rem;
}
h1 {
  margin-left: -5.5rem;
  color: white;
}

#nav {
  background-color: #2e004e;
  background-image: linear-gradient(19deg, #2e004e 0%, #b721ff 100%);
  height: 7rem;
}
#nav ul {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  height: 100%;
}
#nav ul li {
  display: inline-block;
  list-style: none;
  font-size: 2rem;
}
#nav ul li a {
  color: white;
  text-decoration: none;
}
</style>
