<template>
    <div class="flex justify-center">
        <div class="grid grid-rows-2 grid-flow-col overflow-hidden mt-10 rounded-t-lg h-24" style="width:1000px">
            <div class="bg-gray-100 text-slate-500 font-bold pl-5">
                {{title}}
            </div>
            <div class="bg-gray-100 pl-5">
                {{subTitle}}
            </div>
            <div v-if="dizionarioFile.format==='pdf'" class="flex bg-gray-100 text-sm text-gray-500 row-span-2 justify-end pr-10">
                <button type="button" v-on:click="$refs.myPdfComponent.print()">Printa Pdf</button>
                <pdf ref="myPdfComponent" src="./assets/sole_la_nostra_stella.pdf"></pdf>
            </div>         
            <div v-else class="flex bg-gray-100 text-sm text-gray-500 row-span-2 justify-end pr-10">
                {{dizionarioFile.text}}
            </div>
        </div>
    </div>
</template>

<script>
import pdf from 'vue-pdf'
export default {
    components:{
        pdf
    },
    props:{
        title:{
            type:String,
            default:"titolo default"
        },
        subTitle:{
            type:String,
            default:"sottotitolo default"
        },
        dizionarioFile:{
            type:Object,
        }
    }
}

</script>

<style>

</style>