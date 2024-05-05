<script>
export default {
    props: {
        thumb: String,
        price: String,
        series: String,
        type: String
    }
};
</script>

<template>
    <div class="card">
        <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="testo">
        <h4>ACTION</h4>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.card {
    width: 20%;

    img {
        max-width: 100%;
    }

    h4 {
        color: $white-color;
    }
}
</style>