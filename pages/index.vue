<template>
    <div class="container">
        <p class="hello">{{ilman}}</p>
        <p :class="this.class">ini hambin</p>
        <button @click="gantiWarna">klik tombol ini</button>
        <p>{{fayco}}</p>
        <foto class="foto"/>
        <helloworld/>
        <NuxtLink to="/fayco">
            <h1>pindah ke halaman fayco</h1>
        </NuxtLink>
        <button @click="hambin">pencet tombol ini</button>
    </div>
</template>

<script>
import Foto from '../components/foto.vue'
import Helloworld from '../components/Helloworld.vue'
export default {
  components: { Helloworld, Foto },
  data(){
      return{
          ilman: "aku adalah daemon",
          fayco: 90,
          index: [1,2,3,4,5,6],
          class: "merah"
      }
  },
  methods: {
      hambin(){
          this.ilman = "hambin calon kahim hmif"
      },

      gantiWarna(){
          this.class = "hijau"
      }
  }
        
    }
</script>

<style  scoped>
*{
    padding: 0;
    margin: 0;
}

.hello{
    font-size: 40px;
    background-color: red;
    width: 100%;
}

.merah{
    color: red;
    font-size: 40px;
}

.hijau{
    color: green;
    font-size: 40px;
}

@media (min-width: 768px){
    .hello{
        text-align: center;
        background-color: green;
    }
}

</style>