<template>
  <article class="card">
    <a href="#">
      <div class="img-wrapper">
        <img :src="thumb" :alt="title">
      </div>
      <p>{{ title }}</p>
    </a>
  </article>
</template>

<script>
export default {
  name: 'AppSeriesCard',
  props:{
    thumb: String,
    title: String
  }
}
</script>

<style lang="scss" scoped>
  .card{
    width: calc((100% / 6) - 1rem);
    margin: 0 .5rem 1rem;
    a{
      color: white;
    }
    .img-wrapper{
      aspect-ratio: 1/1;
      width: 100%;
      img{
        height: 100%;
        width: 100%;
      }
    }

    p{
      font-size: .8rem;
      font-weight: 400;
    }
  }
</style>