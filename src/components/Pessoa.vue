<template>
<div>
    <h2>Essa é a descrição da pessoa: {{ nome }}</h2>
    <info v-bind:propsEmail="propsEmail"/> <!--props-->
</div>
</template>

<script>
import Info from './Info.vue'
    export default{
  components: {
      Info},
        name:'Pessoa',
        data(){
            return{
                nome: "João",
                propsEmail: 'jhon@gmail.com'
            }
        }
    }

</script>

<style scoped>
    h2{
        margin-top: 20px;
        margin-bottom: 20px;
        text-align: center;  
    }
</style>
