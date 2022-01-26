<template>
<div>
    <p>Imagem de perfil:</p>
  <img :src="avatar" :alt="descricao">
  <MudarImg @mudarImagem="TradeImg" />
</div>
</template>

<script>
import MudarImg from './MudarImg.vue'
export default {
    components:{
        MudarImg
    },
  name: 'Picture',
  data() {
    return { 
      avatar: "/img/avatar.png",
      descricao: "Foto de Perfil"
    }
  },
  methods:{
      TradeImg(){
          this.avatar = "/img/tradeavatar.png"
      }
  }
}
</script>

<style scoped>
img{
    width: 220px;
    height: 220px;
}

</style>