<template>
  <section class="p-index__works l-section">
    <div class="l-container">
      <h2 class="p-index__title">
        WORKS
        <span class="p-index__subtitle">過去の実績</span>
      </h2>

      <carousel :items-to-show="3">
        <slide v-for="work in works" :key="work">
          <WorksCard :works="work" />
        </slide>
      </carousel>
    </div>
  </section>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide } from "vue3-carousel";
import WorksCard from "../../parts/WorksCard.vue";

export default {
  components: {
    Carousel,
    Slide,
    WorksCard,
  },
  data() {
    return {
      works: [
        {
          title: "Sample",
          description: "Worksのサンプルです",
          image: "/images/380x450.png",
        },
        {
          title: "Sample",
          description: "Worksのサンプルです",
          image: "/images/380x450.png",
        },
        {
          title: "Sample",
          description: "Worksのサンプルです",
          image: "/images/380x450.png",
        },
      ],
    };
  },
};
</script>
