<template>
  <div id="app">
    <Header1></Header1>
    <divider titoloCarta="About"></divider>
    <div class="flex justify-center">
      <div class="overflow-hidden rounded-lg text-center mt-10 bg-gray-100 h-10" style="width:1000px">
        Sono un ragazzo di 20 anni che sta studiando per imparare a programmare.
      </div>
    </div>
    <divider titoloCarta="Education"></divider>
    <div v-for="elem in cartaEducation" :key="elem.titolo">
      <carta :title="elem.titolo" :subTitle="elem.sottotitolo" :text="elem.testo"></carta>
    </div>
    <divider titoloCarta="Esperienza"></divider>
    <div v-for="elem in cartaExperience" :key="elem.titolo">
      <carta :title="elem.titolo" :subTitle="elem.sottotitolo" :text="elem.testo"></carta>
    </div>
    <footer class="text-center bg-red-200">Email: vince.lanza01@gmail.com Tel: 3913893652</footer>
  </div>
</template>

<script>
import Header1 from './components/Header.vue'
import carta from './components/Carta.vue'
import divider from './components/divider.vue'

export default {
  components: {Header1,divider,carta},
  data(){
    return{
      cartaEducation: [
        {titolo : "I.T.I.S Galileo Galilei Arezzo", sottotitolo :"Informatica", testo : "15/09/2015-10/06/2020"},
        {titolo : "Scuola media Francesco Severi Arezzo", sottotitolo :"", testo :"14/09/2012-20/06/2015"}
      ],
      cartaExperience: [{
        titolo : "Stage Quinta Superiore", sottotitolo :"Applyx S.r.l.", testo :""},
        {titolo : "Stage Quarta Superiore", sottotitolo :"Applyx S.r.l.", testo :""},
        {titolo : "Stage Terza Superiore", sottotitolo :"Applyx S.r.l.", testo :""}
      ]
    }
  }
}
</script>

<style>
body{
  background-color: rgb(209 213 219);
}
</style>
