<template>
  <div id="app">
    <Header1></Header1>
    <div v-for="elem in carte" :key="elem.primaCarta">
    <carta :title="elem.primaCarta.titolo" :subTitle="elem.primaCarta.sottotitolo" :text="elem.primaCarta.testo"></carta>
    <br>
    <carta :title="elem.secondaCarta.titolo" :subTitle="elem.secondaCarta.sottotitolo" :text="elem.secondaCarta.testo"></carta>
    </div>
  </div>
</template>

<script>
import Header1 from './components/Header.vue'
import carta from './components/Carta.vue'

export default {
  components: {Header1,carta},
  data(){
    return{
      carte: [{primaCarta : {
        titolo : "titolo1", sottotitolo :"sottotitolo1", testo : "testo1"},
        secondaCarta : {
        titolo : "titolo2", sottotitolo :"sottotitolo2", testo : "testo2"},
      }],
    }
  }
}

</script>

<style>
body{
  background-color: lightgrey;
}
</style>
