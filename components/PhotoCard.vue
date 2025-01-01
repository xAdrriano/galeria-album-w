<template>
    <div class="card text-center">
        <img :src="photo.url" :alt="photo.id" class="thumb">           
        <NuxtLink :to="`/photos/${id}-${photo.id}`">      
            <p class="btn my-4 m-2">View Details</p>
        </NuxtLink>
    </div>
</template>

<script setup>
    const { photo } = defineProps(['photo','id'])
</script>

<style scoped>
    .thumb {
        max-height: 200px;
        max-width: 70%;
        margin: 0 auto;
    }
</style>