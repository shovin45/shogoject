<template>
  <div>
    <Nuxt />
    <footer class="footer">
      <p v-if="$route.name != 'index'">
        <nuxt-link class="footer-link" to="/">トップに戻る</nuxt-link>
      </p>
      <small>Created by Shogo Yasumrua</small>
    </footer>
  </div>
</template>

<style lang="scss">
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.footer {
  width: 100%;
  position: fixed;
  bottom: 0px;
  text-align: right;
  padding: 10px;

  @media screen and (max-width: 700px) {
    position: relative;
  }

  p {
    text-align: center;
  }

  &-link {
    display: inline-block;
    margin: 0 auto 30px;
    text-decoration: none;
    color: #333;
  }
}
</style>
