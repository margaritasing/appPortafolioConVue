<template>
<div id="fotter">
    <footer>
        <h3 class="p-4">
            &copy; Libia M Freites M - {{ year }} 
        </h3>
    </footer>
</div>
  
</template>

<script>
export default {
    computed: {
        year(){
            return new Date().getFullYear();
        },
    },

};
</script>

<style scoped>
h3{
    background-color: #6155A6;
    padding: 1rem;
    text-align: center;
    color: #fff;
  }

</style>>

