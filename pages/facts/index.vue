<template>
<div class="container">
  <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke = "joke.joke"/>
</div>
</template>

<script>
import axios from 'axios';
import Joke from "../../components/Jokes";
export default {
  components:{
    Joke
  },
  data:{
    jokes: [],
  },
  async created() {
    const config = {
      headers:{
        'Accept': 'application/json'
      }
    }
    try {
      const res = await axios.get("https://icanhazdadjoke.com/search", config);
      this.jokes = res.data.results;
      console.log(res.data.results)
    }catch (e) {
      console.log(e)
    }
    },
  head(){
    return{
      title:"Random facts"
    }
  }
}
</script>

<style></style>
