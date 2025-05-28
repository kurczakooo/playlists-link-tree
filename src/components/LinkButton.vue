<template>
    <a
        :href="url"
        target="_blank"
        rel="noopener noreferrer"
        class="block w-full text-center py-3 rounded-lg bg-indigo-600 hover:bg-indigo-700 transition-colors text-white font-semibold shadow-md"
    >
        {{ label }}
    </a>
</template>

<script setup>
defineProps({
    label: String,
    url: String,
});
</script>

<style scoped>
/* Możesz dodać dodatkowe style, jeśli chcesz */
</style>
