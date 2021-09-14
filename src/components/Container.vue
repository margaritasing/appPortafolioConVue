<template>
  <div id="container" class="container">
      <h3>Proyectos</h3>
      <img src="https://avatars.githubusercontent.com/u/61855440?v=4" alt="Avatar de Margarita Sing"
      width="100"
      loading="lazy"
      class="image"
      />
      <hr />
      <loading  v-if="load"/>
    <div class="cards" v-for="project in projects" :key="project.id" >
             <Card :name="project.name" 
             :description="project.description"
             :author="project.owner.login"
            :url="project.html_url"
            :homepage="project.homepage" />
     
    </div>
  </div>
</template>

<script>

import Card from"./Card.vue";
import Loading from './Loading.vue';

export default {
    data() {
        return{
            projects: null,
            load: true,
        };
    },

    components:{
        Card,
        Loading,
    },
    mounted(){
        this.getprojects();        
    },
    methods:{
       async getprojects(){
            this.load = true
            const res = await fetch("https://api.github.com/users/margaritasing/repos");
            const data = await res.json();

            this.load =false
            this.projects = data

            console.log(data)
            
           
        },
    },

};
</script>

<style scoped>
.image{
    border-radius: 50%;
}
.cards{
    display: inline-flex;
    flex-wrap: wrap;
    justify-content: center;
   
}
.container{
    background-color: #fff;
    overflow:hidden;
    border: solid 1px #eee;
    box-shadow: 1px 1px 4px #333;
    text-align: center;
}
</style>>

