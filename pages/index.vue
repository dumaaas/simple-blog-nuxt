<template>
  <main>
    <div class="main">
      <div class="main-content">
        <div class="main-content__title">
          <p>DOGS, CATS, AND CODE</p>
          <h1>Hi, I'm <nuxt-link to="/about">Marko Dumnic</nuxt-link> !</h1>
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
          <p>Read some of my <nuxt-link to="/blog">blog posts</nuxt-link> .</p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
main {
  background-color: #1e1e1e;
  height: 100vh;

  a {
    color: inherit;
    background-image: linear-gradient(0deg, #2ec997 50%, transparent 0);
    background-size: 100% 200%;
    background-position: top;
    transition: background-position 0.25s ease-in-out, color 0.25s ease-in-out;
    border-radius: 2px;
    padding: 0 2px;
    border-bottom: 2px solid #2ec997;

    &:hover {
      background-position: bottom;
      color: #000;
    }
  }

  .main {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100vh;
    &-content {
      padding-left: 20px;
      p {
        font-size: 20px;
        line-height: 25px;
        color: #f5f5f5;

        &:not(:first-child) {
          padding-top: 25px;
        }

        a {
          padding: 4px 2px;
        }
      }
      h1 {
        padding-top: 5px;
        font-size: 64px;
        line-height: 72px;
        font-weight: 700px;
        color: #ffffff;
      }
    }
  }
}
</style>
