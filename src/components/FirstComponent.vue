<template>
    <div class="firstcomponent">
        <h1>Olá, estou trabalhando com VueJS</h1>
        <p class="eusou">Eu sou o {{ nome }}</p>
        <MultiplosEventos />
        <p><Reutilizacao /></p>
        <p><Reutilizacao /></p>
        <p><Reutilizacao /></p>
        <p><Reutilizacao /></p>
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'

    export default{
        name: 'FirstComponent',
        components:{
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return{
                nome:"João Eugênio"
            }
        }
    }
</script>

<style scoped>
.firstcomponent{
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
}

.eusou{
        font-size: 25px;
        margin-top: 20px;
        margin-bottom: 20px;
}


</style>

