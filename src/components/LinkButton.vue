<template>
    <a
        :href="url"
        target="_blank"
        rel="noopener noreferrer"
        class="flex items-center gap-5 w-full py-3 px-3 rounded-xl bg-gradient-to-b from-[#2e2e2e] to-gray-90 shadow-[6px_6px_10px_rgba(0,0,0,0.9)]"
    >
        <img
            :src="imagePath"
            alt="playlist thumbnail"
            class="w-20 h-20 rounded-lg"
        />
        <span class="text-l font-bold">{{ label }}</span>
    </a>
</template>

<script setup>
defineProps({
    label: String,
    url: String,
    imagePath: String,
});
</script>
