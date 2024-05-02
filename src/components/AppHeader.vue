<script>
export default {
  data() {
    return {
      menu: [
        {
          title: "Characters",
          isActive: false,
        },
        {
          title: "Comics",
          isActive: true,
        },
        {
          title: "Movies",
          isActive: false,
        },
        {
          title: "Tv",
          isActive: false,
        },
        {
          title: "Games",
          isActive: false,
        },
        {
          title: "Collectibles",
          isActive: false,
        },
        {
          title: "Videos",
          isActive: false,
        },
        {
          title: "Fans",
          isActive: false,
        },
        {
          title: "News",
          isActive: false,
        },
        {
          title: "Shop",
          isActive: false,
        }
      ],
    }
  }
}
</script>

<template>
  <header>
    <div class="container">
      <div class="header-logo">
        <img src="../assets/img/dc-logo.png" alt="Logo DC Comics">
      </div>

      <ul class="header-menu">
        <li v-for="item in menu">
          <a href="#" :class="{ active: item.isActive }"> {{ item.title.toUpperCase() }}</a>
        </li>
      </ul>

    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header {
  @include flex(row, center, center);

  .container {
    @include flex(row, space-between, center);
    width: 80%;
    max-width: 1440px;
    height: 150px;

    .header-menu {
      @include flex(row, space-between, center);
      list-style-type: none;
      gap: 1em;

      li {
        height: 100%;
        display: inline-block;

        a {
          text-decoration: none;
          color: $black-color;

          &:hover {
            color: $primary-color;
          }

          &.active {
            color: $primary-color;
          }
        }
      }

    }
  }
}
</style>