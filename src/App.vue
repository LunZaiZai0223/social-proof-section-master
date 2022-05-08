<template>
  <the-container></the-container>
  <footer>
    <p>
      Challenge by
      <a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
      >Frontend Mentor</a
      >. Coded by
      <a href="https://github.com/LunZaiZai0223" target="_blank"
      >LunZaiZai0223</a
      >.
    </p>
  </footer>
</template>

<script>
import TheContainer from './components/TheContainer.vue';

export default {
  name: 'App',
  components: {
    TheContainer,
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=League+Spartan:wght@400;500;700&family=Noto+Sans+TC:wght@300;400;500&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  overflow: hidden;
  @media screen and (max-width: 768px) {
    overflow-x: hidden;
    overflow-y: auto;
  }
}

ul li {
  list-style-type: none;
}

#app {
  font-family: 'League Spartan', sans-serif;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  @media screen and (max-width: 768px) {
    padding: 2rem 0;
  }
}

footer {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: White;
  text-align: center;
  @media screen and (max-width: 768px) {
    margin-top: 1.5rem;
    position: relative;
  }
}

</style>
