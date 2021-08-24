<template>
  <section>
    <div class="about">
      <div class="about-title">
        <div class="about-title__img">
          <img src="@/assets/images/me.jpg" alt="logo" />
        </div>
        <div class="about-title__heading">
          <h2>About Me</h2>
        </div>
      </div>
      <div class="about-content">
        <p>
          Hey, I'm Marko! I made this template. If you're reading this, you
          should probably be changing the content on this page. You can do that
          in <code>pages/about/index.vue.
              </code>
        </p>
        <p>
          Want to change the image above? (Hopefully!) Add your own in <code>
assets/images
          </code>
          . You can replace mine and title yours <code>me.jpg</code> (or, rename
          it and change the file path above).
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
section {
  height: 100vh;
  background-color: #1e1e1e;
}
.about {
  margin: 0 auto;
  padding: 120px 20px 0 20px;
  max-width: 78ch !important;
  &-title {
    display: flex;
    gap: 15px;
    align-items: center;
    &__img {
      img {
        width: 100px;
        height: 100px;
        border-radius: 50%;
      }
    }
    &__heading {
      h2 {
        font-size: 56px;
        line-height: 84px;
        color: #f5f5f5;
        font-weight: 800;
      }
    }
  }
  &-content {
      p {
          font-size: 19px;
          color: #f5f5f5;
          font-weight: 400;
          line-height: 29px;
          padding-top: 50px;
          &:nth-child(2) {
              padding-top: 20px;
          }
      }
  }
}
</style>