<script>
export default {};
</script>

<template>
  <main>
    <div class="jumbotron"></div>
    <section class="container">
      <div class="label">
        <h2>CURRENT SERIES</h2>
      </div>
      <div class="row">
        <div class="col">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Perspiciatis qui debitis ducimus
          sapiente quaerat. Ad maxime, voluptatibus deserunt natus vel sint, eius illum sequi itaque tenetur minima
          laudantium vitae error.</div>
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
  position: relative;

  .jumbotron {
    width: 100%;
    height: 200px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;
  }

  .container {
    @include flex(row, center, center);
    width: 80%;
    max-width: 1440px;
    height: 150px;
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
      background-color: lightblue;
      height: 100px;

      width: 100%;

      .col {}

    }

  }
}
</style>