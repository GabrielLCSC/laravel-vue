<template>
    <MusicLayout>
        <template #title>
            <h1>Playlists</h1>
        </template>

        <template #action>
            <Link :href="route('playlists.create')" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline">
                Créer une playlist
            </Link>
        </template>

        <template #content>
            <div class="grid grid-cols-3 gap-4">

            </div>
        </template>
    </MusicLayout>
</template>
<script>
import MusicLayout from "@/Layouts/MusicLayout.vue";
export default {
    components: {MusicLayout}
}
</script>
