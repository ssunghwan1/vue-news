<template>
  <div>
      <!-- <div v-for ="user in users">{{user}}</div> -->
  </div>
</template>

<script>
import axios from 'axios';
import
export default {
  data(){
    return {
      users:[]
    }
  },
  created(){
    var vm = this;
    axios.get('https://api.hnpwa.com/v0/news/1.json')
    .then(function(response){
      console.log(response);
      vm.users = response.data;
    })
    .catch(function(error){
      console.log(error)
    })
  },
}
</script>

<style>

</style>