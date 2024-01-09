<template>
    <MusicLayout>
        <template #title> Musiques </template>

        <template #action>
            <Link :href="route('tracks.index')"> Retour </Link>
        </template>
        <template #content> </template>
    </MusicLayout>
</template>

<script>
import { Link } from "@inertiajs/vue3";

import MusicLayout from "@/Layouts/MusicLayout.vue";

export default {
    components: {
        MusicLayout,
        Link,
    },
    props: {},
};
</script>
<style></style>
