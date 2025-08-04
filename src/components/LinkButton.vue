<template>
    <a
        :href="url"
        :id="button_id"
        target="_blank"
        rel="noopener noreferrer"
        @click="trackClick"
        class="flex items-center gap-5 w-full py-3 px-3 rounded-xl bg-gradient-to-b from-[#2e2e2e] to-gray-90 shadow-[6px_6px_10px_rgba(0,0,0,0.9)]"
    >
        <img
            :src="'/covers/' + image_path"
            alt="playlist thumbnail"
            class="w-20 h-20 rounded-lg"
        />
        <span class="text-l font-bold">{{ label }}</span>
    </a>
</template>

<script>
export default {
    props: {
        label: String,
        url: String,
        button_id: String,
        imagePath: String,
    },
    methods: {
        trackClick() {
            if (typeof gtag === 'function') {
                gtag('event', 'button_click', {
                    event_category: 'playlist',
                    event_label: this.button_id,
                    value: 1,
                });
            }
        },
    },
};
</script>
