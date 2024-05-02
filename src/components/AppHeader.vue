<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<template>
    <header>
        <div class="container">
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veritatis, tenetur nobis cupiditate, blanditiis nisi alias fuga, quas nesciunt ut tempore omnis sit maiores? Veniam, ipsa id ipsam temporibus earum excepturi.</p>
        </div>
    </header>
</template>

<style scoped lang="scss">

@use "../style/partials/mixins" as *;

header {
    @include flex(row, center, center);
    
    .container {
        @include flex(row, center, center);
        max-width: 80%;
        background-color: lightcoral;
}
}

</style>