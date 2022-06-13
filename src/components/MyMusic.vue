<template>
  <div id="mycard">
    <div>
        <img :src="CardDisk.poster" :alt="CardDisk.title">
    </div>
    <h1>
        {{CardDisk.title}}
    </h1>
    <div>
        {{CardDisk.author}}
        {{CardDisk.year}}
    </div>
  </div>
</template>

<script>


export default {
  name: 'MyMusic',
  props : {
    CardDisk : Object
  }
}
</script>

<style lang="scss">
    #mycard {
        background-color: #2e3a46;
        display: flex;
        flex-direction: column;
        flex-basis: 15%;
        justify-content: flex-start;
        align-items: center;
        margin: 20px;
        padding: 10px;

        img{
            width: 200px;
            height: 250px;
            object-fit: contain;
        }
        h1{
            color: white;
        }
    }
   

</style>