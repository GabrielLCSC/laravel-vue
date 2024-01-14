<template>
    <div class="card">
        <div class="image__container">
            <img :src="'/storage/' + track.image" alt="test" />
        </div>
        <div class="card__description">
            <div class="flex_illustration">
                <div class="svg__illustration"></div>
                <h3>{{ track.title }}</h3>
            </div>
            <p>{{ track.artist }}</p>
        </div>
        <button @click="handleClick">Lire</button>
        <Link
            v-if="$page.props.isAdmin"
            :href="route('tracks.edit', { track: track })"
            class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline"
        >Modifier
        </Link>
        <Link
            v-if="$page.props.isAdmin"
            :href="route('tracks.destroy', { track: track })"
            method="delete"
            as="button"
            class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline">
        Supprimer
        </Link>
    </div>
</template>
<script>
export default {
    emits: ["played"],
    props: {
        track: Object,
        active: {
            type: Boolean,
            default: false,
        },
    },
    methods: {
        handleClick() {
            this.$emit("played", this.track);
        },
    },
};
</script>
