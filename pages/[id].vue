<template>
    <div class="grid grid-cols-4 gap-5">
        <div v-for="p in photos">
            <PhotoCard :photo="p" :id="id"/>
        </div>
    </div>
</template>

<script setup>

    const { id } = useRoute().params

    const uri = "https://jsonplaceholder.typicode.com/albums/" + id + "/photos"

    const { data: photos } = await useFetch(uri, {key: id })

    useHead({
    title: '| Album - '+ id +' |',
  })
</script>

<style scoped>

</style>