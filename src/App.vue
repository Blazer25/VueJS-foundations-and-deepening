<template>
  <div>
    <Header :props_esta_logado="true"/> <!--props-->
    <First-component />
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
    import Header from './components/Header'
    import FirstComponent from './components/FirstComponent.vue'
    import LifeCycle from './components/LifeCycle.vue'
    import Pessoa from './components/Pessoa.vue'
 
    export default{
      name:'app',
      components:{
        FirstComponent,
        LifeCycle,
        Pessoa,
        Header
      }
    }
</script>

<style>
html{
  --background: #D5F3F4;
  --botoes: #4A9BDD;
  --link: #4F93C8;
}

* {
    margin: 0;
    padding: 0;
    border: none;
    text-decoration: none;
    box-sizing: border-box;
}

body{
  background: var(--background);
}

button{
    width: 200px;
    height: 50px;
    margin-bottom: 14px;
    border: 2px solid black;
    background: var(--botoes);
    margin: 14px;
}
</style>