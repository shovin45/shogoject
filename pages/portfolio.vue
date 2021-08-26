<template>
  <div class="container__portfolio">
    <ul class="item-list">
      <li
        v-for="(work, index) in works"
        :key="index"
        :class="`animate__animated animate__flipInX animate__delay-${index}s`"
      >
        <a class="item-link" :href="work.link" target="_blank">
          <p><img class="caption" :src="work.img" /></p>
          <h3>{{ work.name }}</h3>
        </a>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'

interface Work {
  name: string
  link: string
  img: (url: string) => any
}

export default defineComponent({
  setup() {
    const works = ref<Work[]>([
      {
        name: 'yNTranslations',
        link: 'https://yntranslations.com/',
        img: require('@/assets/shot-yn-min.jpg'),
      },
      {
        name: 'Lucky Strike Web Site',
        link: 'https://www.lucky-strike.jp/',
        img: require('@/assets/shot-luckyhp-min.jpg'),
      },
      {
        name: 'Lucky School Web Site',
        link: 'https://school.lucky-strike.jp/',
        img: require('@/assets/shot-luckyschool-min.jpg'),
      },
      {
        name: 'Lucky Strike メンズダンサー SNSまとめ',
        link: 'https://lucky-strike.netlify.app/',
        img: require('@/assets/shot-luckysns-min.jpg'),
      },
      {
        name: 'The Emmanuelle Sunflower WebSite',
        link: 'https://the-emmanuelle-sunflower.com/',
        img: require('@/assets/shot-emma-min.jpg'),
      },
      {
        name: 'タピオカドリンクのタピや',
        link: 'https://tapiya.com/',
        img: require('@/assets/shot-tapiya-min.jpg'),
      },
    ])
    return {
      works,
    }
  },
})
</script>

<style lang="scss">
.container__portfolio {
  max-width: 1000px;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90vh;

  @media screen and (max-width: 700px) {
    height: auto;
  }
}
.item-list {
  list-style-type: none;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  @media screen and (max-width: 700px) {
    margin: 50px 0;
  }

  li {
    margin: 15px 10px;
    transition: opacity 0.4s;

    &:hover {
      opacity: 0.7;
    }
  }
  .item-link {
    text-decoration: none;
    color: #333;
    font-size: 14px;
  }
}
.caption {
  width: 300px;
}
</style>
