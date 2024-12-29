<template>
    <div v-for="p in photo" class="grid grid-cols-4 gap-5">
        {{ p.title }}
    </div>
</template>

<script setup>


    const { id, albumId } = useRoute().params
    const uri = "https://jsonplaceholder.typicode.com/albums/" + albumId + "/photos?id=" + id
    const { data: photo } = await useFetch(uri, {key: id })
    

</script>

<style scoped>

</style>