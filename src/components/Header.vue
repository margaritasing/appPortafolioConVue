<template>
 <header>
     <h1> {{title}} </h1>
 </header>
</template>

<script>
export default {
  props: {
    title: String,
  },    
};
</script>



<style scoped>
h1{
  background-color: #6155A6;
  padding: 1rem;
  text-align: center;
  color: snow;
}

</style>
