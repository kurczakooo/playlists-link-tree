<template>
    <main
        class="min-h-screen bg-gradient-to-b from-gray-900 to-black text-white flex flex-col items-center px-4 py-10"
    >
        <div class="max-w-md w-full">
            <div class="text-center mb-8">
                <img
                    src="../assets/logo.png"
                    alt="Avatar"
                    class="w-24 h-24 rounded-full mx-auto mb-4 border-4 border-indigo-500"
                />
                <h1 class="text-3xl font-bold">TwojaNazwa</h1>
                <p class="text-sm text-gray-400">
                    Playlisty aktualizowane codziennie
                </p>
            </div>

            <div class="space-y-4">
                <LinkButton
                    label="🔥 Top 100 Polska"
                    url="https://open.spotify.com/playlist/your_playlist_id_1"
                />
                <LinkButton
                    label="🎧 Chill Vibes"
                    url="https://open.spotify.com/playlist/your_playlist_id_2"
                />
                <LinkButton
                    label="🚗 Na drogę"
                    url="https://open.spotify.com/playlist/your_playlist_id_3"
                />
                <LinkButton
                    label="🌍 Global Top 50"
                    url="https://open.spotify.com/playlist/your_playlist_id_4"
                />
            </div>

            <footer class="mt-10 text-xs text-gray-500 text-center">
                &copy; 2025 TwojaNazwa. Powered by Spotify.
            </footer>
        </div>
    </main>
</template>

<script setup>
import LinkButton from './LinkButton.vue';
</script>

<style>
body {
    font-family: 'Inter', sans-serif;
}
</style>
