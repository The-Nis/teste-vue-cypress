<template>
  <div id="app">

    <div class="login-container">
      <input type="text" v-model="login" >
      <input type="password" v-model="senha">
      <button @click="abrir(login, senha)" id="login-btn" >Acessar</button>
    </div>
    
    <label for="" v-if="mostrar" >{{ texto }}</label>

  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data () {
    return {
      login: '',
      senha: '',
      mostrar: false,
      texto: ''
    }
  },
  methods: {
    abrir (login, senha) {
      if(login == 'adm' && senha == '123'){
        this.mostrar = true
        this.texto = 'senha correta'
      } else {
        this.mostrar = true
        this.texto = 'senha incorreta'
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
