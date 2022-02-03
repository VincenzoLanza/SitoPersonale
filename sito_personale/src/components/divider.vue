<template>
   <div class="relative">
      <div class="absolute inset-0 flex items-center z-0">
        <div class="w-full border-t border-gray-400"></div>
      </div>
      <div class="relative flex justify-center">
        <div class="px-3 text-xl font-medium bg-gray-300">{{titoloCarta}}</div>
      </div>
    </div>
</template>

<script>
export default {
    props :{
        titoloCarta :{
            type:String,
            default:"titolo default"
        }
    }
}
</script>

<style>

</style>