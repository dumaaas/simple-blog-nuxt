<template>
  <section>
    <div class="blog">
      <BlogHeading
        :date="date"
        :readingTime="readingTime"
        :title="title"
        :description="description"
      />

      <div class="blog-content">
        <p>
          Welcome! Here's how to write a blog post. (Not how to write, but how
          to write a blog post using this template.) This post is written in
          <a>Markdown</a>. Read the <a>syntax guide</a> to get started using
          Markdown easily.
        </p>
        <h3>Images</h3>
        <p>
          To use an image, write <code>{{ inlineImage }}</code> as you see
          below.
        </p>
        <div class="code">
          <p>
            <span class="tag"
              >&lt;InlineImage <span class="attribute">:src</span
              ><span class="data">="require(`@/assets/images/howToBlog.jpg`)"</span
              ><span class="attribute"> alt</span
              ><span class="data">="Pikachu waving!"</span
              >&gt;&lt;/InlineImage&gt;</span
            >
          </p>
        </div>
        <p>The above outputs the following:</p>
        <InlineImage
          :src="require(`@/assets/images/howToBlog.jpg`)"
          alt="Pikachu waving!"
        />
        <p class="bg-leading pt-20">
          The images (<code>.jpg</code>, <code>.png</code>, <code>.gif</code>)
          that you reference here should live in
          <code>static/post/{post directory}</code>.
        </p>
        <p>(You can also do GIFs):</p>
        <div class="code">
          <p>
            <span class="tag"
              >&lt;InlineImage <span class="attribute">src</span
              ><span class="data">="require(`@/assets/images/pikachuGif.webp`)"</span
              ><span class="attribute"> alt</span
              ><span class="data">="Pikachu waving, in a GIF!</span
              >&gt;&lt;/InlineImage&gt;</span
            >
          </p>
        </div>
        <InlineImage
          :src="require(`@/assets/images/pikachuGif.webp`)"
          alt="Pikachu waving as gif!"
        />
        <h3 class="pt-20">Grids</h3>
        <p>
          By specifying <code>width</code> in an <code>{{ inlineImage }}</code
          > , you can create grid-based layouts:
        </p>
        <div class="code">
          <p>
            <span class="tag"
              >&lt;InlineImage <span class="attribute">src</span
              ><span class="data">="require(`@/assets/images/pokemons.webp`)"</span
              ><span class="attribute"> alt</span
              ><span class="data">="Pikachu waving, in a GIF!</span
              >&gt;&lt;/InlineImage&gt;</span
            >
          </p>
          <p>
            <span class="tag"
              >&lt;InlineImage <span class="attribute">src</span
              ><span class="data">="require(`@/assets/images/pikachuGif.webp`)"</span
              ><span class="attribute"> alt</span
              ><span class="data">="Pikachu waving, in a GIF!</span
              >&gt;&lt;/InlineImage&gt;</span
            >
          </p>
          <p>
            <span class="tag"
              >&lt;InlineImage <span class="attribute">src</span
              ><span class="data">="require(`@/assets/images/pikachuGif.webp`)"</span
              ><span class="attribute"> alt</span
              ><span class="data">="Pikachu waving, in a GIF!</span
              >&gt;&lt;/InlineImage&gt;</span
            >
          </p>
          <p>
            <span class="tag"
              >&lt;InlineImage <span class="attribute">src</span
              ><span class="data">="require(`@/assets/images/pokemons.webp`)"</span
              ><span class="attribute"> alt</span
              ><span class="data">="Pikachu waving, in a GIF!</span
              >&gt;&lt;/InlineImage&gt;</span
            >
          </p>
        </div>

        <InlineImage
          :src="require(`@/assets/images/pokemons.webp`)"
          alt="Pikachu waving as gif!"
          width="49.5%"
        />
        <InlineImage
          :src="require(`@/assets/images/pikachuGif.webp`)"
          alt="Pikachu waving as gif!"
          width="49.5%"
        />
        <InlineImage
          :src="require(`@/assets/images/pikachuGif.webp`)"
          alt="Pikachu waving as gif!"
          width="49.5%"
        />
        <InlineImage
          :src="require(`@/assets/images/pokemons.webp`)"
          alt="Pikachu waving as gif!"
          width="49.5%"
        />
        <h3 class="pt-20">Info boxes</h3>
        <p>
          The <code>{{ infoBox }}</code> component allows you to include quick
          notes in your blog posts.
        </p>
        <div class="code">
          <p>
            <span class="tag">&lt;InfoBox&gt;</span>
          </p>
          <p class="pl-10">
            <span class="tag">&lt;template&gt;</span>
          </p>
          <p class="pl-20">They look like this.</p>
          <p class="pl-10">
            <span class="tag">&lt;/template&gt;</span>
          </p>
          <p>
            <span class="tag">&lt;/InfoBox&gt;</span>
          </p>
        </div>
        <InfoBox>❗ They look like this.</InfoBox>
      </div>

      <hr />
      <BackToAll />
      <OtherBlogs :otherBlogs="otherBlogs"/>
    </div>
  </section>
</template>
<script>
import BlogHeading from "@/components/BlogHeading.vue";
import BackToAll from "@/components/BackToAll.vue";
import InlineImage from "@/components/InlineImage.vue";
import InfoBox from "@/components/InfoBox.vue";
import OtherBlogs from '@/components/OtherBlogs.vue';

export default {
  props: {
    BlogHeading,
    BackToAll,
    InlineImage,
    InfoBox,
    OtherBlogs
  },
  data() {
    return {
      date: "MARCH 2021",
      readingTime: "2 minute read",
      title: "How to Blog",
      description: "Getting started with the Nuxt Blog Starter template.",
      inlineImage: "<InlineImage>",
      infoBox: "<InfoBox>",
      otherBlogs: [
          {
              title: 'Dogs',
              url: 'dogs',
              img: 'dogs.jpg',
              alt: 'Dog blog post',
          }, 
          {
              title: 'Cats',
              url: 'cats',
              img: 'cats.jpg',
              alt: 'Cat blog post'
          }
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  height: 100vh;
  background-color: #1e1e1e;
  overflow-y: auto;
  .bg-leading {
    line-height: 32px !important;
  }
  .pl-10 {
    padding-left: 10px;
  }
  .pl-20 {
    padding-left: 20px;
  }
  .pt-20 {
    padding-top: 20px;
  }

  .blog {
    margin: 0 auto;
    padding: 120px 20px;
    max-width: 78ch !important;

    a {
        color: #2EC997;

        &:hover {
            color: #fff;
            text-decoration: underline;
            transition: all .3 ease-in-out;
        }
    }

    p {
      font-size: 18px;
      line-height: 26px;
      color: #f5f5f5;
      font-weight: 400;
      padding-bottom: 20px;
    }

    h3 {
      padding-bottom: 15px;
      font-size: 22px;
      line-height: 34px;
      font-weight: 700;
      color: #f5f5f5;
    }

    .code {
      margin-bottom: 20px;
      background-color: #0f0f0f;
      padding: 15px 20px;
      border-radius: 5px;
      p {
        font-family: monospace;
        font-size: 14px;
        line-height: 21px;
        padding-bottom: 0;
      }

      .tag {
        color: #96cbfe;
      }

      .attribute {
        color: #a8ff60;
      }

      .data {
        color: #f9ee98;
      }
    }
  }
}
</style>