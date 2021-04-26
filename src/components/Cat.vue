<template>
  <div id="cat" class="">
 
    <div v-if="cats.length === 0">Loading...</div>
    <div v-if="cats && cats.length" class="cat-continer pt-28">
      <ul  class="flex flex-wrap justify-between" >
        <li v-for="cat of cats" :key="cat.id" class="card mb-12	" >
          <div class="img-card">
              <img v-bind:src='cat.image && cat.image.url' :alt='cat.name' /> 
          </div>   
          <div class="p-8">
            <h2 class="text-xl pb-2.5" >
            {{cat.name}}
          </h2> 
          <h4 class="text-gray-400 py-1.5">{{cat.origin}}</h4>
          <p class="text-sm text-gray-500"> {{cat.description}} </p>
            </div>     
                 
        </li>
      </ul>
    </div>
    <div>

    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      cats: [],
      errors: [],
    };
  },
  mounted() {
    axios
      .get("https://api.thecatapi.com/v1/breeds")
      .then((res) => {
        this.cats = res.data;
      })
      .catch((err) => {
        this.errors.push(err);
      });
  },
};
</script>

<style scoped>

#cat {
  background: #f1f1f1;
}
.cat-continer{
  width: 90%;
  margin: 0 auto;
}
.card{
  width: 31%;
  background: #fff;
  border-radius: .6rem;
}
.img-card{
height: 250px;

}
.img-card img{
  border-top-left-radius: .6rem;
  border-top-right-radius: .6rem;
  width: 100%;
  height: 100%;
}
</style>
