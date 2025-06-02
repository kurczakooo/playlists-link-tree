<template>
    <main
        class="min-h-screen bg-gradient-to-b from-gray-900 to-black text-white flex flex-col items-center px-4 py-10"
    >
        <div class="max-w-md w-full">
            <div class="text-center mb-8">
                <img
                    src="../assets/logo.png"
                    class="w-24 h-24 bg-gradient-to-r from-purple-600 to-teal-400 mx-auto mb-4 rounded-full"
                />
                <h1 class="text-3xl font-bold">Pulse Beats</h1>
            </div>

            <div class="space-y-4">
                <LinkButton
                    v-for="(playlist, index) in playlists"
                    :key="index"
                    :label="playlist.label"
                    :url="playlist.url"
                    :imagePath="playlist.imagePath"
                />
            </div>
        </div>
    </main>
</template>

<script setup>
import LinkButton from '../components/LinkButton.vue';
import { ref, onMounted } from 'vue';

const playlists = ref([]);

onMounted(async () => {
    const response = await fetch('/playlists.json');
    playlists.value = await response.json();
});
</script>
