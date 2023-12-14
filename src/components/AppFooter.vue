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
         <button>sign up now!</button>
          <nav>
            <button>follow us</button>
            <ul>
              <li>
                <img :src="getImageUrl(path)" alt="">
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
      path: 'footer-facebook.png',
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
      socialsLink[
        {
          path: 'footer-facebook.png',
          link: '#'
        }
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
  background-color: $footer-bg;
}
</style>