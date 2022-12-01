<template>
  <section class="our-services mt-20 flex flex-col items-center">
    <div class="title-box flex items-center flex-col">
      <h2 class="font-semibold text-4xl text-center">Our services</h2>
      <p class="text-center my-10 flex justify-center px-5">
        We provides to you the best choices for you. Adjust it to your health
        needs and make sure your undergo treatment with our highly qualified
        doctors you can consult with us which type of service is suitable for
        your health
      </p>
    </div>
    <div
      class="services grid grid-cols-custom gap-10 justify-center mt-10 px-7 mb-16 relative"
    >
      <img src="../../../assets/element.png" class="absolute right-12 -z-10 top-0 bottom-0 my-auto" alt="">
      <div>
        <img src="../../../assets/seek.png" alt="" />
        <h3 class="text-2xl text-black font-bold my-4">Search a doctor</h3>
        <p>
          Choose your doctor from thousands of specialist, general, and trusted
          hospitals
        </p>
      </div>
      <div>
        <img src="../../../assets/remedy.png" alt="" />
        <h3 class="text-2xl text-black font-bold my-4">Online pharmacy</h3>
        <p>
          Buy your medicines with our mobile application with a simple delivery
          system
        </p>
      </div>
      <div>
        <img src="../../../assets/tablet.png" alt="" />
        <h3 class="text-2xl text-black font-bold my-4">Consultation</h3>
        <p>
          Free consultation with our trusted doctors and get the best
          recomendations
        </p>
      </div>
      <div>
        <img src="../../../assets/health.png" alt="" />
        <h3 class="text-2xl text-black font-bold my-4">Details info</h3>
        <p>
          Free consultation with our trusted doctors and get the best
          recomendations
        </p>
      </div>
      <div>
        <img class="mb-9" src="../../../assets/bag.png" alt="" />
        <h3 class="text-2xl text-black font-bold my-4">Emergency care</h3>
        <p>
          You can get 24/7 urgent care for yourself or your children and your
          lovely family
        </p>
      </div>
      <div>
        <img src="../../../assets/track.png" alt="" />
        <h3 class="text-2xl text-black font-bold my-4">Tracking</h3>
        <p>Track and save your medical history and health data</p>
      </div>
    </div>
    <!-- <div class="btn-container"> -->
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
          w-[180px]
          text-center
        "
        >Learn more</a
      >
    <!-- </div> -->
  </section>
</template>
<script>
</script>
<style scoped>
.our-services {
  background: url("../../../assets/back.png") no-repeat;
  background-size: 50%;
  background-position-y: 320px;
}
.title-box {
  margin-bottom: 2rem;
}
.title-box h2 {
  position: relative;
  padding: 2rem;
}
.title-box h2:after {
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

.title-box p {
  max-width: 832px;
  color: #7d7987;
}


.services div {
  box-shadow: 10px 40px 50px rgba(229, 233, 246, 0.4);
  background-color: #fff;
  padding: 1.8rem;
  border-radius: 20px;
}

.services {
  width: 100%;
  max-width: 1240px;
}
.services div p {
  color: #7d7987;
}

.learn {
  border: 1px solid #458ff6;
  color: #458ff6;
  transition: ease 0.4s all;
}

.learn:hover {
  background-color: #458ff6;
  color: white;
}

.btn-container {
  width: 100%;
  height: max-content;
  display: flex;
  justify-content: center;
}
</style>