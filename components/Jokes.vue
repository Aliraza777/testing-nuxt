<template>
  <div class="Joke">
  <p>{{joke}} </p>
  </div>
</template>

<script>
export default {
  name : 'Joke',
  props:[
    'joke' , 'id'
  ]
}
</script>

<style>
.Joke{
  padding: 1rem;
  border: 1px solid #ccc;
  margin: 1rem 0;
}
</style>
