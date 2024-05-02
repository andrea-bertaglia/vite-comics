<script>
export default {
  data() {
    return {
      dcComicsMenu: ["Characters", "Comics", "Movies", "Tv", "Games", "Videos", "News"],
      shopMenu: ["Shop DC", "Shop DC Collectibles"],
      dcMenu: ["Terms Of Use", "Privacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
      sitesMenu: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"],
    }
  }
}
</script>

<template>
  <footer>
    <section class="footer-top">
      <div class="container">

        <div class="top-left">
          <div class="col">
            <div>
              <span>DC COMICS</span>
              <ul>
                <li v-for="item in dcComicsMenu"><a href="#">{{ item }}</a></li>
              </ul>
            </div>
            <div>
              <span>SHOP</span>
              <ul>
                <li v-for="item in shopMenu"><a href="#">{{ item }}</a></li>
              </ul>
            </div>

          </div>

          <div class="col">
            <span>DC</span>
            <ul>
              <li v-for="item in dcMenu"><a href="#">{{ item }}</a></li>
            </ul>
          </div>

          <div class="col">
            <span>SITES</span>
            <ul>
              <li v-for="item in sitesMenu"><a href="#">{{ item }}</a></li>
            </ul>
          </div>


        </div>





        <div class="top-right">
          <img src="../assets/img/dc-logo-bg.png" alt="Logo DC Comics Grande">
        </div>
      </div>
    </section>

    <section class="footer-bottom">
      <div class="container">
        <div class="bottom-left">
          <a href="#">SIGN-UP NOW!</a>
        </div>
        <div class="bottom-right">
          <span>FOLLOW US</span>
          <a href="#">
            <img src="../assets/img/footer-facebook.png" alt="Logo Facebook">
          </a>
          <a href="">
            <img src="../assets/img/footer-twitter.png" alt="Logo Twitter">

          </a>
          <a href="">
            <img src="../assets/img/footer-youtube.png" alt="Logo Youtube">

          </a>
          <a href="">
            <img src="../assets/img/footer-pinterest.png" alt="Logo Pinterest">

          </a>
          <a href="">
            <img src="../assets/img/footer-periscope.png" alt="Logo Periscope">

          </a>
        </div>
      </div>
    </section>

  </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

footer {
  @include flex(column, center, center);
  color: $white-color;

  .footer-top {
    @include flex(column, center, center);
    background-image: url("../assets/img/footer-bg.jpg");
    width: 100%;
    height: 300px;


    .container {
      @include flex(row, space-between, center);
      width: 80%;
      max-width: 1440px;

      .top-left {
        @include flex(row, flex-start, flex-start);
        width: 100%;

        .col {
          width: 33%;

          li {
            list-style-type: none;
            font-size: .8rem;
            padding: .3em 0;

            a {
              text-decoration: none;
              color: $grey-color;
            }
          }

          span {
            font-size: 1.1rem;
            font-weight: bold;
          }
        }

      }

      .top-right {
        width: 90%;

        img {
          max-width: 100%;
        }
      }
    }


  }

  .footer-bottom {
    @include flex(column, center, center);
    background-color: $secondary-color;
    width: 100%;
    height: 100px;
    position: relative;


    .container {
      @include flex(row, space-between, center);
      width: 80%;
      max-width: 1440px;

      .bottom-left {

        a {
          border: .2em solid $primary-color;
          padding: .5em;
          color: $white-color;
          text-decoration: none
        }
      }

      .bottom-right {
        @include flex(row, space-between, center);
        gap: 1em;

        span {
          color: $primary-color;
          font-weight: bold;
          font-size: 1.1rem;
        }

      }
    }


  }

}
</style>