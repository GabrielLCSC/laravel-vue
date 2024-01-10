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
