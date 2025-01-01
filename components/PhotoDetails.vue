<template>
    <div class="card">     
        <div class="grid grid-cols-2 gap-10">
            <div class="p-7">
                <img :src="photo.url" :alt="photo.id" class="mx-auto my-7">   
            </div>
            <div class="p-7">
                <h2 class="text-4xl my-7 border-b-2">Title: {{ photo.title }}</h2>
            </div>
        </div>       
    </div>
</template>

<script setup>
    const { photo } = defineProps(['photo','id'])
</script>

<style scoped>
    img {
        max-width: 600px;
    }
</style>