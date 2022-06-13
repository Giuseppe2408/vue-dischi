<template>
    <header>
        <img src="https://i.kinja-img.com/gawker-media/image/upload/s--ypN6iH9q--/c_fill,fl_progressive,g_center,h_900,q_80,w_1600/zrarqnhmkoaihvzss5ek.jpg" alt="">
    </header>
</template>

<script>
export default {
  name: 'MyHeader',
  
}
</script>

<style lang="scss">

    header{
        height: 70px;
        background-color: #1b1414;
        img {
            border-radius: 50%;
            object-fit: contain;
            width: 70px;
            height: 70px;
        }
    }

</style>