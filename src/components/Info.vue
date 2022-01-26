<template>
    <div class="all_info">
    <h2 v-if="esta_trabalhando">Ela, a pessoa, trabalha com:</h2>
    <p v-else>Ela trabalha com:</p>
  <ul>
    <li v-for="(tec, index) in back_trabalha_com" v-bind:key="index">{{ tec }}</li>
  </ul>

  <ul>
      <li v-for="tec in front_trabalha_com" :key="tec.id">
          {{tec.language}}
      </li>
  </ul>
  <div>
      <button @click="showEmail">{{ textoEmail }}</button>
  </div>

  <p class="email_margin" v-show="mostrar_email">Mande um email para: joao@hotmail.com</p>
  <p class="email_margin" v-show="mostrar_email">Meu segundo email é  {{ propsEmail }}</p>

  <p>Para acessar meu site, <a v-bind:href="meu_link"> clique aqui</a></p>  
  <Picture />
    </div>
</template>

<script>
import Picture from './Picture'

    export default{
        name:'Info',
        components:{
            Picture
        },
        props:{
            propsEmail: String
        },
        data(){
            return{
                esta_trabalhando: false,
                mostrar_email: false,
                meu_link: 'https://google.com',
                textoEmail: "Mostrar email",
                back_trabalha_com: ["JavaScript","PHP","NodeJS"],
                front_trabalha_com: [
                    {id: 1, language: 'CSS3'},
                    {id: 2, language: 'Bootstrap5'},
                    {id: 3, language: 'HTML5'},
                    {id: 4, language: 'VueJS'}
                ]
            }
        },
        methods:{
            showEmail(){

                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email)
                {
                    this.textoEmail = "Mostrar email"
                } else {
                    this.textoEmail = "Esconder email"
                }
            }
        }
    }
</script>

<style scoped>
    a{
        color: var(--link);
    }

    .all_info{
        font-size: 25px;
        margin-top: 20px;
        margin-bottom: 20px;
        text-align: center;
    }

    .email_margin{
        margin: 15px;
    }
</style>
