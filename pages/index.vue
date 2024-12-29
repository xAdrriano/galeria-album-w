<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="a in albumy">
                <NuxtLink :to="`/${a.id}`">{{ a.title }}</NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
    const { data: albumy } = await useFetch('https://jsonplaceholder.typicode.com/albums')
</script>

<style scoped>

</style>