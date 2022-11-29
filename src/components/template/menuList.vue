<template>    
    <div>
        <div v-for="p in picture" :key="p"> 
            <h2>{{p.name}}</h2>
            <div class="menuImg">
                <img :src="`${p.image}`" alt="">
            </div>
            <div v-for="i in p.ingredients" :key="i">
                {{i}},
            </div>
    </div>
    </div>
</template>
<script setup>
import {ref, onBeforeMount} from "vue";
import axios from "axios";


const picture = ref([]);
onBeforeMount(async () => {
  picture.value = await pictures();
}); 
const pictures = async () => {
    let options = {
  method: 'GET',
  url: 'https://recipesapi2.p.rapidapi.com/recipes/tomato%20soup',
  params: {maxRecipes: '5'},
  headers: {
    'X-RapidAPI-Key': 'ad9b5bf13fmshc4ae85653eb100bp1f1cebjsn0c1891767137',
    'X-RapidAPI-Host': 'recipesapi2.p.rapidapi.com'
  }
};


let stoba = await axios.request(options)
  return stoba.data.data;
};
</script>
<style scoped>
.menuImg img{
    height: 100px;
    width: 100px;
}
</style>
