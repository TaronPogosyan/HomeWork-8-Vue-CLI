<template>
  <section class="blog center">
    <p class="blog__title">Articles & News</p>
    <p class="blog__text">
      It is a long established fact that a reader will be distracted by the of
      readable content of a page when lookings at its layouts the points of
      using.
    </p>
    <div class="blog__items">
      <BlogCard v-for="item in homeBlogData" :key="item.id" :text="item" />
    </div>
  </section>
</template>

<script>
import BlogCard from "@/components/BlogCard.vue";
export default {
  name: "HomeBlog",

  components: {
    BlogCard,
  },

  mounted() {},

  methods: {},

  data() {
    return {
      homeBlogData: [
        {
          id: 1,
          src: require("../assets/img-art-01.png"),
          alt: "photo",
          class: "blog__item_img",
          tag: "Kitchan Design",
          title: "Let’s Get Solution For Building Construction Work",
          date: "26 December,2022",
        },
        {
          id: 2,
          src: require("../assets/img-art-02.png"),
          alt: "photo",
          class: "blog__item_img",
          tag: "Living Design",
          title: "Low Cost Latest Invented Interior Designing Ideas.",
          date: "22 December,2022",
        },
        {
          id: 3,
          src: require("../assets/img-art-03.png"),
          alt: "photo",
          class: "blog__item_img",
          tag: "Interior Design",
          title: "Best For Any Office & Business Interior Solution",
          date: "25 December,2022 ",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.blog {
  margin-bottom: 96px;

  &__title {
    margin-bottom: 10px;
    color: #292f36;
    text-align: center;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 1px;
  }

  &__text {
    margin-bottom: 52px;
    width: 811px;
    margin-left: auto;
    margin-right: auto;
    color: #4d5053;
    text-align: center;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.22px;
  }

  &__items {
    display: flex;
    flex-direction: row;
    gap: 25px;
    flex-wrap: wrap;
  }
}
</style>
