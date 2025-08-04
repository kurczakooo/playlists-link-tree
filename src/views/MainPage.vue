<template>
    <main
        class="min-h-screen bg-[linear-gradient(to_bottom_left,_#393939_5%,_#222222_25%,_#111111_70%)] text-white flex flex-col items-center px-4 py-10"
    >
        <div class="max-w-md w-full">
            <div class="text-center mb-6">
                <img
                    src="../assets/logo.png"
                    class="w-24 h-24 mx-auto mb-4 rounded-full shadow-[0_0_80px_15px_rgba(29,185,84,0.4)]"
                />
                <h1 class="text-4xl font-bold">Pulse Beats</h1>
            </div>

            <div class="flex justify-center gap-20 mb-9">
                <!-- Spotify -->
                <a
                    href="https://open.spotify.com/user/31fsanywwop5iabf5f46gab2dtsm?si=86ae452487824e30"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    <img
                        src="../assets/spotify_logo.png"
                        alt="TikTok"
                        class="w-10 h-10 rounded-full bg-[rgba(29,185,84,0.15)] shadow-[0_0_16px_8px_rgba(29,185,84,0.2)]"
                    />
                </a>

                <!-- Instagram -->
                <a
                    href="https://www.instagram.com/pulsebeatsofficial"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    <img
                        src="../assets/ig_logo.png"
                        alt="TikTok"
                        class="w-10 h-10 rounded-xl bg-[rgba(198,47,148,0.15)] shadow-[0_0_16px_8px_rgba(198,47,148,0.2)]"
                    />
                </a>

                <!-- TikTok -->
                <a
                    href="https://www.tiktok.com/@pulsebeatsofficial"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    <img
                        src="../assets/tiktok_logo.png"
                        alt="TikTok"
                        class="w-10 h-10 rounded-full bg-[rgba(105,201,208,0.15)] shadow-[0_0_16px_8px_rgba(105,201,208,0.2)]"
                    />
                </a>
            </div>

            <div class="space-y-4">
                <LinkButton
                    v-for="(playlist, index) in playlists"
                    :key="index"
                    :label="playlist.label"
                    :url="playlist.url"
                    :button_id="playlist.button_id"
                    :image="playlist.image"
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
