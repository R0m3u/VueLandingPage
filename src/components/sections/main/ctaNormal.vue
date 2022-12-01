<template>
  <section
    class="cta-one mt-32 flex justify-evenly flex-wrap items-center max-w-[1280px] m-auto" :class="css"
  >
    <img class="w-[75%] md:w-[470px]" :src="link" alt="" />
    <div class="max-w-[438px] px-6 mt-16 md:m-0">
      <h3 class="font-bold text-4xl leading-[56px]">
        {{ title }}
      </h3>
      <p class="text-base md:text-lg text-[#7D7987] font-light leading-8 my-8 max-w-[450px]">
        {{text}}
      </p>
      <a
        href="#"
        class="
          learn
          btn
          transition-all
          ease-out
          duration-400
          px-10
          py-3
          rounded-full
          border border-[#458ff6]
          text-[#458ff6]
          border-cyan-500
          hover:text-white hover:bg-[#458ff6]
          block
          w-max
          max-w-[163px]
          flex
          justify-between
          items-center
        "
        >{{ btnTxt }} 
        <!-- <img :class="none" class="ml-3 hover:fill-white" :src="icon" /> -->
        <div :class="none" class="flex items-center ml-3">
          <svg class="h-[14px]" width="11" height="15" viewBox="0 0 11 16" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M4.81951 1.05554L4.81951 12.6308L2.27646 10.0877C1.92569 9.73698 1.39954 9.73698 1.04878 10.0877C0.698014 10.4385 0.698014 10.9647 1.04878 11.3154L5.08258 15.3492C5.43335 15.7 5.95949 15.7 6.31026 15.3492L10.3441 11.3154C10.6948 10.9647 10.6948 10.4385 10.3441 10.0877C9.9933 9.73698 9.46715 9.73698 9.11638 10.0877L6.57333 12.6308L6.57333 1.05554C6.57333 0.617083 6.22257 0.178627 5.69642 0.178627C5.17027 0.178627 4.81951 0.617083 4.81951 1.05554Z" fill="#458FF6"/>
          </svg>            
        </div>
          
        </a
      >
    </div>
  </section>
</template>

<script>
    export default {
      props: ['link', 'title', 'text', 'css', 'btnTxt', 'none', 'icon']
    }
</script>
f
<style scoped>
.cta-one div h3 {
  position: relative;
  padding-bottom: 1.4rem;
}

.cta-one div h3:after {
  position: absolute;
  content: "";
  height: 3px;
  width: 50px;
  left: 0;
  background-color: black;
  bottom: 0;
}

.learn div {
  height: 14px;
}
.learn:hover div > svg > path {
  fill: #fff;
}
</style>