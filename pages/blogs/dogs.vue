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
          The domestic dog (Canis familiaris or Canis lupus familiaris) is a
          domesticated form of wolf. The dog descended from an ancient, extinct
          wolf, with the modern wolf being the dog's nearest living relative.
          The dog was the first species to be domesticated by hunter–gatherers
          more than 15,000 years ago, prior to the development of agriculture.
          Their long association with humans has led dogs to be uniquely attuned
          to human behavior, enabling an abundant cosmopolitan distribution and
          to be able to thrive on a starch-rich diet that would be inadequate
          for other canids.
        </p>
        <p>
          The dog has been selectively bred over millennia for various
          behaviors, sensory capabilities and physical attributes. Dogs are
          subclassified into breeds, which vary widely in shape, size and color.
          They perform many roles for humans, such as hunting, herding, pulling
          loads, protection, assisting police and the military, companionship,
          therapy and aiding disabled people. This influence on human society
          has given them the sobriquet of "man's best friend."
        </p>
      </div>
      <hr />
      <BackToAll />
      <OtherBlogs :otherBlogs="otherBlogs" />
    </div>
  </section>
</template>

<script>
import BlogHeading from "@/components/BlogHeading.vue";
import BackToAll from "@/components/BackToAll.vue";
import OtherBlogs from "@/components/OtherBlogs.vue";
export default {
  props: {
    BlogHeading,
    BackToAll,
    OtherBlogs,
  },
  data() {
    return {
      date: "JANUARY 2021",
      readingTime: "1 minute read",
      title: "Dogs",
      description: "Dogs are the best animal. Here's why.",
      otherBlogs: [
        {
          title: "How to Blog",
          url: "welcome",
          img: "howToBlog.jpg",
          alt: "How to Blog post",
        },
        {
          title: "Cats",
          url: "cats",
          img: "cats.jpg",
          alt: "Cat blog post",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  height: 100vh;
  background-color: #1e1e1e;
  overflow-y: auto;
}
.blog {
  margin: 0 auto;
  padding: 120px 20px;
  max-width: 78ch !important;
}
p {
  font-size: 18px;
  line-height: 26px;
  color: #f5f5f5;
  font-weight: 400;
  &:last-child {
    padding-top: 20px;
  }
}
</style>