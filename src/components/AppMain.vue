<script>
export default {};
</script>

<template>
  <main>
    <section class="container">
      <h2>==>Content goes here<== </h2>
    </section>

  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

main {
  @include flex(row, center, center);

  .container {
    @include flex(row, center, center);
    width: 100%;
    max-width: 1440px;
    height: 150px;
    background-color: $black-color;

    h2 {
      color: $white-color;
    }
  }
}
</style>