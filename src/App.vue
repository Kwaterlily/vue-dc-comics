<template>
  <div>
    <BaseHeader />
    <TheMain />
    <BaseSection />
    <BaseFooter />
    <BaseFooterBottom />  
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue';
import TheMain from './components/TheMain.vue';
import BaseSection from './components/BaseSection.vue';
import BaseFooter from './components/BaseFooter.vue';
import BaseFooterBottom from './components/BaseFooterBottom.vue';


export default {
  name: 'vue-dc-comics',
  components: {
    BaseHeader,
    TheMain,
    BaseSection,
    BaseFooter,
    BaseFooterBottom
  },
};
</script>

<style>
/* Generics */
  * {
    margin:0;
    padding:0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Raleway', sans-serif;
  }

  img {
    heaght: auto;
    max-width: 100%;
  }

  ul {
    list-style-type: none;
  }

  a {
    color: #000;
    text-decoration: none;
  }

  /* Utils */
  .container {
    margin: 0 auto;
    max-width: 1200px;
  }

</style>
