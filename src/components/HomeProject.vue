<template>
  <section class="project center">
    <p class="project__title">Follow Our Projects</p>
    <p class="project__text">
      It is a long established fact that a reader will be distracted by the of
      readable content of page lookings at its layouts points.
    </p>
    <div class="project__items">
      <ProjectCard
        v-for="item in projectCardData"
        :key="item.id"
        :text="item"
        :sizeButton="70"
      />
      <!-- <HomeProjectCard /> -->
    </div>
  </section>
</template>

<script>
// import HomeProjectCard from './HomeProjectCard.vue';
import ProjectCard from "@/components/ProjectCard.vue";

export default {
  name: "HomeProject",
  mounted() {},
  methods: {},
  components: {
    // HomeProjectCard,
    ProjectCard,
  },
  data() {
    return {
      projectCardData: [
        {
          id: "product-card1",
          src: require("../assets/product-01.png"),
          alt: "image",
          title: "Modern Kitchan",
          subtitleLeft: "Decor",
          subtitleLine: " / ",
          subtitleRight: "Artchitecture",
        },
        {
          id: "product-card2",
          card_id: "bedroom",
          src: require("../assets/product-02.png"),
          alt: "image",
          title: "Modern Kitchan",
          subtitleLeft: "Decor",
          subtitleLine: " / ",
          subtitleRight: "Artchitecture",
        },
        {
          id: "product-card3",
          card_id: "bedroom",
          src: require("../assets/product-03.png"),
          alt: "image",
          title: "Modern Kitchan",
          subtitleLeft: "Decor",
          subtitleLine: " / ",
          subtitleRight: "Artchitecture",
        },
        {
          id: "product-card4",
          card_id: "bedroom",
          src: require("../assets/product-04.png"),
          alt: "image",
          title: "Modern Kitchan",
          subtitleLeft: "Decor",
          subtitleLine: " / ",
          subtitleRight: "Artchitecture",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.project {
  margin-top: 96px;

  &__title {
    color: #292f36;
    text-align: center;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    /* 62.5px */
    letter-spacing: 1px;
  }

  &__text {
    margin-top: 8px;
    margin-bottom: 93px;
    width: 737px;
    margin-left: auto;
    margin-right: auto;
    color: #4d5053;
    text-align: center;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 33px */
    letter-spacing: 0.22px;
  }

  &__items {
    display: grid;
    grid-template-columns: repeat(2, auto);
    column-gap: 104px;
    row-gap: 56px;
    margin-bottom: 96px;
  }

  // &__item {
  //     display: grid;
  //     gap: 24px;

  //     &_content {
  //         display: flex;
  //         gap: 260px;

  //         &-title {
  //             color: #292F36;
  //             font-family: DM Serif Display;
  //             font-size: 25px;
  //             font-style: normal;
  //             font-weight: 400;
  //             line-height: 125%;
  //             /* 31.25px */
  //             letter-spacing: 0.5px;
  //         }

  //         &-subtitle {
  //             width: 217px;
  //             height: 27px;
  //             color: #4D5053;
  //             font-family: Jost;
  //             font-size: 22px;
  //             font-style: normal;
  //             font-weight: 400;
  //             line-height: 150%;
  //             /* 33px */
  //             letter-spacing: 0.22px;
  //         }
  //     }
  // }
}
</style>
