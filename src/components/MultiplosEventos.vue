<template>
    <div>
        <button @click="primeiro($event), segundo($event), tecerio($event)">Ativar múltiplos eventos</button>
        <p> {{ multiplos_eventos }} </p>
    </div>
</template>

<script>
export default {
    name: 'MultiplosEventos',
    data(){
        return{
        multiplos_eventos: ""
        }
    },
    methods:{
        primeiro(){
            this.multiplos_eventos = "1° Evento ativado"
        },
        segundo(){
            setTimeout(() => this.multiplos_eventos = "2° Evento", 4000)
        },
        teceiro(){
            setTimeout(() => this.multiplos_eventos = "", 500)
        }
    }
    }
</script>

<style scoped>

</style>