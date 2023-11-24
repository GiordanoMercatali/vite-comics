<script>

export default {
  props: {
    propThumb: String,
    propPrice: String,
    propSeries: String,
    propType: String
  },
};
</script>

<template>
  <div class="card">
    <img :src="propThumb" alt="" />
    <h3>{{ propSeries }}</h3>
    <p>{{ propPrice }}</p>
  </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
.card {
    background-color: white;
    height: 100%;

    img {
        width: 10rem;
        height: 15rem;
    }

    h3 {
        text-align: center;
        color: $primary-color;
    }

    /* &.comic-book {
        background-color: lightblue;
    }

    &.graphic-novel  {
        background-color: lightgreen;
    } */
}
</style>