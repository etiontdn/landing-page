<template>
  <div id="app" class="has-background-backgroundcolor">
    <Navbar></Navbar>
    <transition name="page" class="test">
      <PageContent v-if="isLoaded" id="pagecontent"></PageContent>
    </transition>
    <Footer></Footer>
  </div>
</template>

<script>
import PageContent from './components/PageContent.vue';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  data: function () {
    return {
      isLoaded: false
    }
  },
  components: {
    PageContent,
    Navbar,
    Footer,
  },
  mounted: function (){
    this.isLoaded = true;
  },
};


</script>

<style lang="scss">
@import 'main.scss';
.page-enter-active, .page-leave-active {
  transition: opacity 0.5s;
}
.page-enter, .page-leave-to {
  opacity: 0;
}

#app {
  font-family: 'Rubik', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  .title {
    font-family: 'Rubik Mono One', sans-serif;
  }
}

.button {
  &:active {
    transform: scale(0.96);
  }
}

body {
  min-width: 320px;
}
@import '~bulma';
@import '~buefy/src/scss/buefy';
</style>
