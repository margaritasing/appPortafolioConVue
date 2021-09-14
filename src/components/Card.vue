<template>
  <div class="row">
        <div class="col-sm-3">
           <div class="card">
            <div class="card-body">
                <h4 class="card-title">{{ name }}</h4> 
                <p class="card-text">{{ description }}</p>
                <p class="card-text"><strong>{{ author }}</strong></p>
                <button-url :url="url"  />
                <button-url color="red" :url="homepage" v-if="homepage != null" title="Deploy"/>               
            </div>
        </div>
    </div>
</div>
 
</template>

<script>
import ButtonUrl from './ButtonUrl.vue'
export default {
  components: { ButtonUrl },
    props:{
        name: String,
        description: String,
        author: String,
        url: String,
        homepage: String,
        
    }

}
</script>

<style scoped>
.card{
    width: 270px;
    height: 300px;
    margin: 7px;
    border: solid 1px #eee;
    box-shadow: 1px 1px 4px #333;
    text-align: center;
}



.card-title{
    font-size: 20px;
}

</style>