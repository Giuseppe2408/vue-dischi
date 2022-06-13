<template>
  <div id="list"> 
    <MyMusic 
    v-for="(disk, i) in mydisk"
    :key="i"
    :CardDisk="disk"/>
  </div>
</template>

<script>
import axios from 'axios'
import MyMusic from './MyMusic.vue'

export default {
  name: 'MyList',
  components : {
    MyMusic
  },
  data(){
    return {
        apiUrl : "https://flynn.boolean.careers/exercises/api/array/music",
        mydisk : []
    }
  },
  created(){
    axios.get(this.apiUrl).then(result =>{
        this.mydisk = result.data.response;
        console.log(result);
    })
  }
}
</script>

<style lang="scss">

    #list{
        height: calc(100vh -  70px);
        background-color: #1e2d3b;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }

</style>