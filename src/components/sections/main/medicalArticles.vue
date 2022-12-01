<template>
  <section
    class="articles mt-12 mx-auto relative"
  >
    <h3 class="title font-semibold text-4xl text-center mb-24">Check out our latest article</h3>
    <div class=" max-w-[900px] mx-auto flex flex-wrap justify-center md:justify-between flex-wrap relative">
        <card class="" :image="data.card1.image" :title="data.card1.title" :text="data.card1.text"/>
        <card :image="data.card2.image" :title="data.card2.title" :text="data.card2.text"/>
        <card :image="data.card3.image" :title="data.card3.title" :text="data.card3.text" class="mb-0"/>
        <img src="../../../assets/element.png" class="hidden md:block absolute -z-10 -top-9 -left-11" alt="">
    </div>
    <img src="../../../assets/back2.png" class="hidden md:block absolute top-[125px] bottom-0 my-0 right-0 -z-10 md:w-[380px]" alt="">
    <a
        href="#"
        class="
          learn
          btn
          transition
          ease-out
          duration-400
          px-10
          py-3
          rounded-full
          text-center

          block
          mt-16
          mx-auto
        "
        >View all</a
      >
</section>
</template>

<script>

import card from "../main/articlesCard.vue";
import cardData from "../../data/cardsData.vue";

export default {
  data() {
    return {
        data: cardData.data().cardsContent,
    };
  },
  components: {
    card,
  },
};
</script>

<style scoped>
.articles .title {
    position: relative;
    padding: 2rem;
  }
  .articles .title:after {
    position: absolute;
    content: "";
    height: 2px;
    width: 50px;
    background-color: #000;
    left: 0;
    right: 0;
    margin: 0 auto;
    bottom: 0;
  }

  .learn {
    border: 1px solid #458ff6;
    color: #458ff6;
    width: 163px;
    transition: ease 0.4s all;
    text-align: center;

  }

  .learn:hover {
    background-color: #458ff6;
    color: white;
  }
</style>
