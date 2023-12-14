<template lang="">
  <header>
    <div class="logo-cont">
      <img src="../assets/img/dc-logo.png" alt="DC logo">
    </div>
    <nav>
      <ul>
        <li v-for="link in navLinks" :class="{'active': link.isActive}">
          <a :href="link.link" :class="{'active': link.isActive}">{{ link.title }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>
<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      navLinks: [
        {
          title: 'characters',
          link: '#',
          isActive: false
        },
        {
          title: 'comics',
          link: '#',
          isActive: true
        },
        {
          title: 'movies',
          link: '#',
          isActive: false
        },
        {
          title: 'tv',
          link: '#',
          isActive: false
        },
        {
          title: 'games',
          link: '#',
          isActive: false
        },
        {
          title: 'collectibles',
          link: '#',
          isActive: false
        },
        {
          title: 'videos',
          link: '#',
          isActive: false
        },
        {
          title: 'fans',
          link: '#',
          isActive: false
        },
        {
          title: 'news',
          link: '#',
          isActive: false
        },
        {
          title: 'shop',
          link: '#',
          isActive: false
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header{
  @include flex(row, space-between, center);
  width: $base-width;
  margin: 0 auto;
  height: 120px;

  div.logo-cont{
    height: 80px;
    img{
      object-position: center;
      object-fit: contain;
      height: 100%;
    }
  }
}

nav {
  font-weight: 500;
  height: 100%;
  ul{
    height: 100%;
    @include flex(row, flex-end, stretch);
    list-style: none;
    li {
      @include flex(row, center, center);
      height: 100%;
      margin-left: 1rem;
      border-bottom: 5px solid transparent;
      &.active {
        border-bottom: 5px solid $accent-color;
      }

      &:hover{
        border-bottom: 5px solid $accent-color;
      }

      a {
        text-transform: uppercase;
        text-decoration: none;
        color: $black;

        &.active {
          color: $accent-color;
        }
      }
    }
  }
}
</style>