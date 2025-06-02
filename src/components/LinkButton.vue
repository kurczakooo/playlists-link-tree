<template>
    <a
        :href="url"
        target="_blank"
        rel="noopener noreferrer"
        class="flex items-center gap-4 w-full py-3 px-4 rounded-lg bg-indigo-600 hover:bg-indigo-700 transition-colors text-white font-semibold shadow-md"
    >
        <img
            :src="imagePath"
            alt="playlist thumbnail"
            class="w-12 h-12 rounded-md object-cover"
        />
        <span class="text-lg">{{ label }}</span>
    </a>
</template>

<script setup>
defineProps({
    label: String,
    url: String,
    imagePath: String,
});
</script>

<style scoped></style>
