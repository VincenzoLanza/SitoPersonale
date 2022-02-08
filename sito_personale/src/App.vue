<template>
  <div id="app">
    <Header1></Header1>
    <divider titoloCarta="About" id="About"></divider>
    <div class="flex justify-center">
      <div class="overflow-hidden rounded-lg text-center mt-10 bg-gray-100 h-10" style="width:1000px">
        Sono un ragazzo di 20 anni che sta studiando per imparare a programmare.
      </div>
    </div>
    <divider titoloCarta="Education" id="Education"></divider>
    <div v-for="elem in cartaEducation" :key="elem.titolo">
      <carta :title="elem.titolo" :subTitle="elem.sottotitolo" :dizionarioFile="elem.testo"></carta>
    </div>
    <divider titoloCarta="Experience" id="Experience"></divider>
    <div v-for="elem in cartaExperience" :key="elem.titolo">
      <carta :title="elem.titolo" :subTitle="elem.sottotitolo" :dizionarioFile="elem.testo"></carta>
    </div>
    <div class="flex justify-center">
      <modale v-if="showModal" @close="showModal = false"></modale>
      <button v-on:click="showModal = true" id="showModal">
        Show Modal
      </button>
      <transition name="modal">
      </transition>
      </div>
    <footer class="text-center bg-red-200" id="Contacts" >Email: vince.lanza01@gmail.com Tel: 3913893652</footer>
  </div>
</template>

<script>
import Header1 from './components/Header.vue'
import carta from './components/Carta.vue'
import divider from './components/divider.vue'
import Modale from './components/Modale.vue'

export default {
  components: {Header1,divider,carta, Modale},
  data(){
    return{
      cartaEducation: [
        {titolo : "I.T.I.S Galileo Galilei Arezzo", sottotitolo :"Informatica", testo : {text: "/home/aidia/Downloads", format: "pdf"}},
        {titolo : "Scuola media Francesco Severi Arezzo", sottotitolo :"", testo : {text: "14/09/2012-20/06/2015", format: "txt"}}
      ],
      cartaExperience: [{
        titolo : "Stage Quinta Superiore", sottotitolo :"Applyx S.r.l.", testo :{text: "/home/aidia/Downloads", format: "pdf"}},
        {titolo : "Stage Quarta Superiore", sottotitolo :"Applyx S.r.l.", testo :{text: "/home/aidia/Downloads", format: "pdf"}},
        {titolo : "Stage Terza Superiore", sottotitolo :"Applyx S.r.l.", testo :{text: "/home/aidia/Downloads", format: "pdf"}}
      ],
      showModal : false
    }
  }
}
</script>

<style>
body{
  background-color: rgb(209 213 219);
  
}
</style>
