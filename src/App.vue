<template>
<div id="app">
  <Header title ="GH Portafolio" />
  <Container /> 
  <Footer />
</div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Container from "./components/Container.vue";
export default {
  components:{
    Header,
    Footer,
    Container,
  },
};
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Glory:wght@300&display=swap');
*{
  margin: 0;
  padding: 0;
  font-family: 'Glory', sans-serif;
}

</style>




