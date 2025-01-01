<template>
    <div>
        <h1 class="font-bold m-2 text-5xl">Albums titles:</h1>
        <div class="grid grid-cols-2 gap-6 font-bold m-4 ">
            <div v-for="a in albumy">
                <NuxtLink :to="`/${a.id}`">{{ a.title }}</NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
    const { data: albumy } = await useFetch('https://jsonplaceholder.typicode.com/albums')

    useHead({
    title: '| Album gallery |',
  })

</script>

<style scoped>

</style>