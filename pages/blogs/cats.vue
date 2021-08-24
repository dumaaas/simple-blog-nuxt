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
          The cat (Felis catus) is a domestic species of small carnivorous
          mammal. It is the only domesticated species in the family Felidae and
          is often referred to as the domestic cat to distinguish it from the
          wild members of the family. A cat can either be a house cat, a farm
          cat or a feral cat; the latter ranges freely and avoids human contact.
          Domestic cats are valued by humans for companionship and their ability
          to hunt rodents. About 60 cat breeds are recognized by various cat
          registries.
        </p>
        <p>
          The cat is similar in anatomy to the other felid species: it has a
          strong flexible body, quick reflexes, sharp teeth and retractable
          claws adapted to killing small prey. Its night vision and sense of
          smell are well developed. Cat communication includes vocalizations
          like meowing, purring, trilling, hissing, growling and grunting as
          well as cat-specific body language. A predator that is most active at
          dawn and dusk, the cat is a solitary hunter but a social species. It
          can hear sounds too faint or too high in frequency for human ears,
          such as those made by mice and other small mammals. It secretes and
          perceives pheromones.
        </p>
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
import OtherBlogs from '@/components/OtherBlogs.vue';
export default {
  props: {
    BlogHeading,
    BackToAll,
    OtherBlogs
  },
  data() {
    return {
      date: "DECEMBER 2020 ",
      readingTime: "2 minute read",
      title: "Cats",
      description: "Cats are the second best animal. Here's why.",
      otherBlogs: [
        {
          title: "How to Blog",
          url: "welcome",
          img: "howToBlog.jpg",
          alt: "How to Blog post",
        },
        {
          title: "Dogs",
          url: "dogs",
          img: "dogs.jpg",
          alt: "Dogs blog post",
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