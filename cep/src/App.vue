<script >
export default {
  data()  {
    return{
      cep: " ",
      resultado: {}
    };
  },
};
methods: {
  async buscar()  {
    const url=''
    this.resultado = await axios.get(url, {
      headers: {}
      Authorization: "Token token"
    )
  }
}
</script>

<template>
  <main>
    <h1>Busca CEP</h1>
    <form @submit.prevent="search">
    <input type="text" v-model="cep" />
    <button type="submit">Buscar</button>
    </form>
      
  </main>
  </template>