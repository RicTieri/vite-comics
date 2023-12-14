<template lang="">
  <footer>
    <section class="up-footer">
      <div class="wrapper">
        <nav>
          <div>
            <ul v-for="link in pageLinks">
              <h2>{{ link.title }}</h2>
              <li v-for="link in link.links">
                <a :href="link.link">{{ link.name }}</a>
              </li>
            </ul>
          </div>
          <ul>
            <h2>{{ aboutUs.title }}</h2>
            <li v-for="link in aboutUs.links">
              <a :href="link.link">{{ link.name }}</a>
            </li>
          </ul>
          <ul>
            <h2>{{ referralLink.title }}</h2>
            <li v-for="link in referralLink.links">
              <a :href="link.link">{{ link.name }}</a>
            </li>
          </ul>
        </nav>
        <div class="bg-logo">
          <!-- <img src="../assets/img/dc-logo-bg.png" alt="bg-logo dc"> -->
        </div>
      </div>
    </section>
    <section class="down-footer">
      <div class="wrapper">
         <button class="btn-bordered">sign-up now!</button>
          <nav>
            <button>follow us</button>
            <ul>
              <li v-for="social in socialsLink">
                <a :href="social.link">
                  <img :src="getImageUrl(social.path)" :alt="social.name">
                </a>
              </li>
            </ul>
          </nav>
        </div>
      </section>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
  data() {
    return {
      pageLinks: [
        {
          title: 'dc comics',
          links: [
            {
              name: 'Characters',
              link: '#'
            },
            {
              name: 'Comics',
              link: '#'
            },
            {
              name: 'Movies',
              link: '#'
            },
            {
              name: 'TV',
              link: '#'
            },
            {
              name: 'Games',
              link: '#'
            },
            {
              name: 'Videos',
              link: '#'
            },
            {
              name: 'News',
              link: '#'
            },
          ]
        },
        {
          title: 'shop',
          links: [
            {
              name: 'Shop DC',
              link: '#'
            },
            {
              name: 'Shop DC Collectibles',
              link: '#'
            }
          ]
        },
      ],
      aboutUs: {
        title: 'dc',
        links: [
          {
            name: 'Terms Of Use',
            link: '#'
          },
          {
            name: 'Privacy policy (New)',
            link: '#'
          },
          {
            name: 'Ad Choices',
            link: '#'
          },
          {
            name: 'Advertising',
            link: '#'
          },
          {
            name: 'Jobs',
            link: '#'
          },
          {
            name: 'Subscriptions',
            link: '#'
          },
          {
            name: 'Talent Workshops',
            link: '#'
          },
          {
            name: 'CPSC Certificates',
            link: '#'
          }, {
            name: 'Ratings',
            link: '#'
          }, {
            name: 'Shop Help',
            link: '#'
          }, {
            name: 'Contact Us',
            link: '#'
          },
        ]
      },
      referralLink: {
        title: 'sites',
        links: [
          {
            name: 'DC',
            link: '#'
          },
          {
            name: 'MAD Magazine',
            link: '#'
          },
          {
            name: 'DC Kids',
            link: '#'
          },
          {
            name: 'DC Universe',
            link: '#'
          },
          {
            name: 'DC Power Visa',
            link: '#'
          }
        ]
      },
      socialsLink:[
        {
          name: 'facebook',
          path: 'footer-facebook.png',
          link: '#'
        },
        {
          name: 'twitter',
          path: 'footer-twitter.png',
          link: '#'
        },
        {
          name: 'youtube',
          path: 'footer-youtube.png',
          link: '#'
        },
        {
          name: 'pinterest',
          path: 'footer-pinterest.png',
          link: '#'
        },
        {
          name: 'periscope',
          path: 'footer-periscope.png',
          link: '#'
        },
      ]
    }
  },
  methods: {
    getImageUrl: function(path) {
      return new URL(`../assets/img/${path}`, import.meta.url).href;
    }
  },
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

footer {
  color: $white;
  background-image: url(../assets/img/footer-bg.jpg);
  background-size: cover;

  .wrapper {
    width: $base-width;
    margin: 0 auto;
    @include flex(row, flex-start, stretch)
  }
}

.up-footer {
  // padding: 2rem 0;
  width: 100%;

  .wrapper {
    justify-content: space-between;

    nav {
      padding: 2rem 0;
      @include flex(row, flex-start, stretch);

      ul {
        list-style: none;
        margin: 0 3rem 2rem 0;

        h2 {
          font-weight: 400;
          text-transform: uppercase;
          margin-bottom: 1rem;
        }

        li {
          margin-bottom: .25rem;

          a {
            font-size: .9rem;
            color: #959595;
          }
        }
      }
    }

    .bg-logo {
      width: 600px;
      background-image: url(../assets/img/dc-logo-bg.png);
      background-position: center;
      background-size: cover;
      overflow: hidden;

      img {}
    }
  }



}

.down-footer {
  padding: 2rem 0;
  background-color: $footer-bg;

  .wrapper{
    justify-content: space-between;

    button{
      text-transform: uppercase;
      background: transparent;
      border: none;
      font-weight: 600;
    }
    .btn-bordered{
      color: $white;
      padding: .5rem 1rem;
      border: 2px solid $accent-color;
    }
  
    nav{
      @include flex(row, flex-end, center);
      
      button{
        font-size: 1.1rem;
        color: $accent-color;
      }

      ul{
        @include flex(row, flex-end, center);
        list-style: none;

        li{
          margin-left: 1.5rem;
        }
      }
    }
  }
}
</style>