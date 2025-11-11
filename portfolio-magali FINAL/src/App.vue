<template>
  <div id="app">
    <Header />
    <MainContent />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import MainContent from './components/MainContent.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainContent,
    Footer
  }
}
</script>

<style>
:root {
  --beige: #F5F5DC;
  --violeta-pastel: #C8A2C8;
  --coral-pastel: #FFB6C1;
  --violeta-oscuro: #6A4C93;
  --texto-oscuro: #333333;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Quicksand', sans-serif;
  background-color: var(--beige);
  color: var(--texto-oscuro);
  line-height: 1.6;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>