<template>
        <img :src="require('@/assets/spinning-globe.gif')" alt="spinning globe gif" loop class="globe-gif">
</template>



<script>

export default{
    name: "Globe-gif"
}

</script>



<style>
.globe-gif{
    border-radius: 55%;
    width: 35%;
    height: auto;
    aspect-ratio: 1/1;
    
}

@media only screen and (max-width: 600px){
  .globe-gif{
    width: 90%
  }
}

</style>