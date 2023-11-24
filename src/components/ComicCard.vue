<script>

export default {
  props: {
    propThumb: string,
    propPrice: string,
    propSeries: string,
    propType: string
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
        width: 100%;
    }

    h3 {
        text-align: center;
        color: $primary;
    }

    /* &.comic-book {
        background-color: lightblue;
    }

    &.graphic-novel  {
        background-color: lightgreen;
    } */
}
</style>