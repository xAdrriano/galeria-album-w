<template>
    <div v-for="p in photo">
        <PhotoDetails :photo="p"/>
    </div>
</template>

<script setup>


    const { id, albumId } = useRoute().params
    const uri = "https://jsonplaceholder.typicode.com/albums/" + albumId + "/photos?id=" + id
    const { data: photo } = await useFetch(uri, {key: id })
    
    useHead({
    title: '| Album - '+ albumId +' | Photo - ' + id + ' |',
  })
</script>

<style scoped>

</style>