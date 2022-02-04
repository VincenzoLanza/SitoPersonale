<template>
    <div class="flex justify-center">
        <div class="grid grid-rows-2 grid-flow-col overflow-hidden mt-10 rounded-t-lg h-24" style="width:1000px">
            <div class="bg-gray-100 text-slate-500 font-bold pl-5">
                {{title}}
            </div>
            <div class="bg-gray-100 pl-5">
                {{subTitle}}
            </div>
            <div class="flex bg-gray-100 text-sm text-gray-500 row-span-2 justify-end pr-10">
                {{text}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        title:{
            type:String,
            default:"titolo default"
        },
        subTitle:{
            type:String,
            default:"sottotitolo default"
        },
        text:{
            type:String,
            default:"testo default"
        }
    },
}
</script>

<style>

</style>