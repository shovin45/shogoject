<template>
  <div class="container">
    <p class="animate__animated animate__flipInY">
      <picture class="profile-img">
        <source
          class="profile-img"
          type="image/webp"
          srcset="~/assets/shogo.jpg.webp"
          width="300"
          height="300"
        />
        <img
          class="profile-img"
          src="~/assets/shogo.jpg"
          alt=""
          width="300"
          height="300"
        />
      </picture>
    </p>
    <div>
      <h2 class="profile-text animate__animated animate__zoomInLeft">
        踊れるエンジニア
      </h2>
      <p
        class="
          profile-text
          animate__animated animate__zoomInUp animate__delay-1s
        "
      >
        こんにちは。<br />shogoです。<br />フリーのWebエンジニアをしてます。<br />ダンスもしています。<br /><br />Web制作はもちろん、<br />映像編集やデザイン制作も実績あり。
      </p>
    </div>
  </div>
</template>

<style lang="scss">
.profile-text {
  text-align: center;
}
.profile-img {
  width: 300px;
  border-radius: 500px;
  margin: 0 30px 0 0;

  @media screen and (max-width: 700px) {
    margin: 0;
  }
}
</style>
