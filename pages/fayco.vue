<template>
    <div>
        <p class="fayco">ini halaman punya fayco</p>
        <helloworld/>
        <NuxtLink to="/">kembali</NuxtLink>
    </div>
</template>

<script>
import Helloworld from '../components/Helloworld.vue'
    export default {
  components: { Helloworld },
        
    }
</script>

<style  scoped>
.fayco{
    font-size: 100px;
}
</style>