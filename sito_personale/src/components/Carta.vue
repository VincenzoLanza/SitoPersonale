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
                <object data="/files/sole_la_nostra_stella.pdf" type="application/pdf" v-if="controllo==true">
                    <iframe src="/files/sole_la_nostra_stella.pdf" style='height: 100%; width: 100%;' frameborder="0" scrolling="no"></iframe>
                </object>
                <button type="button" v-on:click="controllo=true">Printa Pdf</button>             
            </div>         
            <div v-else class="flex bg-gray-100 text-sm text-gray-500 row-span-2 justify-end pr-10">
                {{dizionarioFile.text}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            controllo : false
        }
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