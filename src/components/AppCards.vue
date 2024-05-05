<script>
export default {
    props: {
        thumb: String,
        series: String,
    }
};
</script>

<template>
    <div class="card">
        <img :src="`${thumb}`" :alt="`${series}`">
        <h4>{{ series.toUpperCase() }}</h4>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.card {
    padding-bottom: 1em;

    img {
        max-width: 100%;
        aspect-ratio: 1;
    }

    h4 {
        padding-top: .5em;
        color: $white-color;
        font-size: .6rem;
    }
}
</style>