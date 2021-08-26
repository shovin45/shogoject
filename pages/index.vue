<template>
  <div class="container">
    <div class="box">
      <h1 class="main-title animate__animated animate__backInDown">
        <Logo />
      </h1>
      <h2 class="main-title animate__animated animate__backInUp">
        shogo yasumura
      </h2>
      <nav>
        <ul class="nav-menu">
          <li v-for="(text, key) in buttons" :key="key">
            <nuxt-link
              class="links animate__animated animate__fadeInBottomLeft"
              :to="key"
            >
              {{ text }}
            </nuxt-link>
          </li>
        </ul>
      </nav>
      <ul class="sns-list animate__animated animate__backInUp">
        <li v-for="(sns, key) in snsLists" :key="key">
          <a :href="sns.link" target="_blank">
            <img :src="sns.icon" :alt="key" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Logo from '~/components/Logo.vue'

export default Vue.extend({
  components: {
    Logo,
  },
  data() {
    return {
      buttons: {
        portfolio: 'ポートフォリオ',
        profile: 'プロフィール',
      },
      snsLists: {
        twitter: {
          link: 'https://twitter.com/shogogo45',
          icon: require('@/assets/icon-twitter-black.svg'),
        },
        instagram: {
          link: 'https://www.instagram.com/shovin_45/',
          icon: require('@/assets/icon-instagram-black.svg'),
        },
        facebook: {
          link: 'https://www.facebook.com/shogo.yasumura',
          icon: require('@/assets/icon-facebook-black.svg'),
        },
      },
    }
  },
})
</script>

<style lang="scss">
.container {
  min-height: 90vh;
  font-family: 'M PLUS Rounded 1c', sans-serif;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  @media screen and (max-width: 700px) {
    min-height: 80vh;
  }
}

.box {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
  align-items: center;

  nav {
    flex-basis: 100%;
    margin: 60px 0 0 0;
  }
}

.main-title {
  flex-basis: 100%;
  text-align: center;
}
h2 {
  display: block;
  margin: 30px 0 0 0;
}

.nav-menu {
  list-style-type: none;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  margin: auto;
  width: 60%;
  @media screen and (max-width: 700px) {
    display: block;
  }

  li {
    @media screen and (max-width: 700px) {
      margin: 30px auto 0;
      text-align: center;

      &:first-child {
        margin: 0 auto;
      }
    }
  }
}

.links {
  display: inline-block;
  color: #fff;
  padding: 10px 30px;
  background: #026c00;
  box-shadow: 5px 5px 100px rgba(1, 72, 0, 0.15);
  border-radius: 100px;
  text-decoration: none;
}

.sns-list {
  display: flex;
  list-style-type: none;
  margin: 20px 0 0 0;
  padding: 0;

  li {
    padding: 20px 10px 0;

    img {
      width: 20px;
    }
  }
}
</style>
