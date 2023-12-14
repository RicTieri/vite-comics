<template lang="">
  <section>
    <div class="wrapper">
      <ul>
        <li v-for="link in section">
          <div>
            <img :src="getImageUrl(link.path)" alt="link.name">
          </div>
          <a :href="link.link">{{link.name}}</a>
        </li>
      </ul>
    </div>
  </section>
</template>
<script>
export default {
  name: 'AppBanner',
  data() {
    return {
      section:[
        {
          path:'buy-comics-digital-comics.png',
          link:'#',
          name:'digital comics'
        },
        {
          path:'buy-comics-merchandise.png',
          link:'#',
          name:'dc merchandise'
        },
        {
          path:'buy-comics-subscriptions.png',
          link:'#',
          name:'subscription'
        },
        {
          path:'buy-comics-shop-locator.png',
          link:'#',
          name:'comic shop locator'
        },
        {
          path:'buy-dc-power-visa.svg',
          link:'#',
          name:'dc power visa'
        },
      ]
    }
  },
  methods: {
    getImageUrl: function (path) {
      return new URL(`../assets/img/${path}`, import.meta.url).href;
    }
  }
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

section{
  background-color: $accent-color;

  .wrapper{
    width: $base-width;
    margin: 0 auto;
    ul{
      @include flex(row, space-around, center);
      list-style: none;
      height: 100px;
      li{
        @include flex(row, center, center);
        div{
          height: 50px;
          width: 50px;
          margin-right: 1rem;
          img{
            width: 100%;
            height: 100%;
            object-fit: contain;
          }
        }
      }
    }
  }
  a{
    text-transform: uppercase;
    color: $white;
  }
}

</style>