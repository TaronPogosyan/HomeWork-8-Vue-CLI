<template>
  <section class="intro">
    <IntroText class="intro__title" :text="item" v-for="item in blogIntro" />
  </section>
</template>

<script>
import IntroText from "@/components/IntroText.vue";

export default {
  name: "BlogIntro",
  data() {
    return {
      blogIntro: [
        {
          id: "blogText",
          title: "Articles & News",
          subheadLeft: "Home",
          linkLeft: "/",
          subheadLine: " / ",
          subheadRight: "Blog",
          linkRight: "/blog",
        },
      ],
    };
  },
  mounted() {},
  methods: {},
  components: {
    IntroText,
  },
};
</script>

<style lang="scss" scoped>
.intro {
  margin-top: 45px;
  background-image: url("../assets/blog_intro-picture.png");
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;

  &__title {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px 78px;
    width: 503px;
    margin-top: 179px;
    border-radius: 37px 37px 0px 0px;
    background-color: #fff;
  }
}
</style>
