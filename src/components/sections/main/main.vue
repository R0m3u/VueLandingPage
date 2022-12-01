<template>
  <main>
    <heroSection />
    <ourServices />
    <ctaNormal
      :title="dt.cta1.title"
      :text="dt.cta1.text"
      :link="dt.cta1.link"
      :btn-txt="dt.cta1.buttonTxt"
      :none="dt.cta1.none"
    />
    <ctaNormal
      :title="dt.cta2.title"
      :text="dt.cta2.text"
      :link="dt.cta2.link"
      :css="dt.cta2.reverse"
      :btn-txt="dt.cta2.buttonTxt"
      :icon="dt.cta2.icon"
    />
    <carouselComment />
    <medicalArticles/>
  </main>
</template>
<script>
import heroSection from "./heroSection.vue";
import ourServices from "./ourServices.vue";
import ctaNormal from "./ctaNormal.vue";
import ctaData from "../../data/ctaData.vue";
import carouselComment from "./carouselComment.vue";
import medicalArticles from "./medicalArticles.vue";

export default {
  name: "MainContainer",

  data() {
    return {
      dt: ctaData.data(),
    };
  },

  components: {
    heroSection,
    ourServices,
    ctaNormal,
    carouselComment,
    medicalArticles,
  },
};
</script>
<style></style>
