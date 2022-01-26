<template>
    <p>Eu gosto de {{ nome }}</p>
</template>

<script>
export default{
    name: 'LifeCycle',
    data(){
        return{
            nome: "Ainda não sei"
        }
    },
    created(){
        setTimeout(() => {
        this.nome = "Trabalho em equipe"
}, 3000)
    },
    mounted(){
        this.nome = "Jourge"
    }
}

</script>


<style scoped>
    p{
        font-size: 25px;
        margin-top: 20px;
        margin-bottom: 20px;
        text-align: center;
    }
</style>