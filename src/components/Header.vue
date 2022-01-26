<template>
  <div class="cabecalho">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Projetos</a></li>
      <li><a href="#">Contato</a></li>
      <li><a v-if="props_esta_logado" href="#">Meu Perfil</a></li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'Header',
    props:["props_esta_logado"]

  }
</script>

<style scoped>

 ul {
    list-style: none;
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    padding: 20px;
    background:darkblue;
  }
  a {
    color: #DDD;
    text-decoration: none;
    transition: .5s;
    font-size: 20px;
  }
  a:hover {
    color: black;
  }
</style>