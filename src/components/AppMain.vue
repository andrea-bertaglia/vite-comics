<script>
import AppCards from "../components/AppCards.vue"
export default {
  components: {
    AppCards
  },
  data() {
    return {
      comicsArray: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
};
</script>

<template>
  <main>
    <div class="jumbotron"></div>
    <section class="container">
      <div class="label">
        <h2>CURRENT SERIES</h2>
      </div>
      <div class="row">
        <div class="col" v-for="comic in comicsArray">
          <AppCards :thumb="comic.thumb" :series="comic.series" />
        </div>
        <div class="btn">

          <a href="#" class="btn">LOAD MORE</a>
        </div>
      </div>
    </section>

  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

main {
  @include flex(column, center, center);
  background-color: $secondary-black-color;

  .jumbotron {
    width: 100%;
    height: 200px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;
  }

  .container {
    @include flex(row, center, center);
    padding-top: 3em;
    width: 80%;
    max-width: 1440px;
    position: relative;

    .label {
      width: 100%;
      position: absolute;
      top: -15px;
      margin-bottom: 1em;

      h2 {
        display: inline-block;
        background-color: $primary-color;
        color: $white-color;
        padding: .3em .6em;
        font-size: 1.2rem;
      }
    }

    .row {
      @include flex(row, space-between, stretch);
      flex-wrap: wrap;
      gap: 1em;
      width: 100%;

      .col {
        width: calc(100% / 6 * 1 - 1em);
      }

    }

    .btn {
      width: 100%;
      text-align: center;
      padding-bottom: 1.5em;

      a {
        color: $white-color;
        background-color: $primary-color;
        text-decoration: none;
        padding: .7em 4em;
        font-size: .7rem;
        font-weight: bold;

      }
    }

  }
}
</style>