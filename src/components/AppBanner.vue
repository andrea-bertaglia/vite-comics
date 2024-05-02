<script>
export default {
    data() {
        return {
            banner: [
                {
                    path: "comics-digital-comics.png",
                    name: "DIGITAL COMICS",
                },
                {
                    path: "comics-merchandise.png",
                    name: "DC MERCHANDISE",
                },
                {
                    path: "comics-subscriptions.png",
                    name: "SUBSCRIPTION",
                },
                {
                    path: "comics-shop-locator.png",
                    name: "COMIC SHOP LOCATOR",
                },
                {
                    path: "dc-power-visa.svg",
                    name: "DC POWER VISA",
                },

            ],
        }
    },
    methods: {
        getImagePath(imageName) {
            return new URL(`../assets/img/buy-${imageName}`, import.meta.url).href
        },
    }
};
</script>

<template>
    <main>
        <section class="container">

            <div class="col" v-for="item in banner">
                <img :src="getImagePath(item.path)">
                <span>{{ item.name }}</span>
            </div>


        </section>

    </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

main {
    @include flex(row, center, center);
    background-color: $primary-color;
    position: relative;


    .container {
        @include flex(row, center, center);
        width: 80%;
        max-width: 1440px;
        height: 150px;

        .col {
            @include flex(row, center, center);
            width: calc(100% / 5 * 1);

            img {
                max-width: 30%;
                padding-right: .5em;
            }

            span {
                color: $white-color;
                font-size: .8rem;
            }
        }
    }
}
</style>