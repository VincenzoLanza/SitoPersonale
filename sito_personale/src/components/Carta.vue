<template>
    <div class="flex justify-center">
        <div class="max-w-sm overflow-hidden rounded-lg shadow-2xl">
            <header class="bg-gray-100 rounded-t-lg font-bold text-2xl py-5 px-8">{{title}}</header>
            <div class="py-5 px-8 text-center bg-gray-100">
                <p>{{subTitle}}</p>
            </div>
            <footer class="rounded-b-lg bg-gray-100 text-sm text-gray-500 px-8 py-3 text-right">{{text}}</footer>
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