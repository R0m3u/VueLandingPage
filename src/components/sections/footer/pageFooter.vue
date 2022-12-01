<template>
  <footer class="mt-36 relative">
    <img src="../../../assets/element.png" class="absolute bottom-0 -left-6">
    <div class="max-w-[980px] mx-auto footer-box text-white flex items-center justify-between md:justify-around px-8 py-10 md:py-10 flex-wrap">
      <div clas="box1">
        <div class="flex item-center">
            <p
            class="font-bold bg-white h-10 w-10 text-white text-2xl text-center leading-[2.5rem] rounded-full text-[#5B9BF3]"
          >
            T
          </p>
          <p class="leading-[40px] ml-[10px] text-[24px] font-bold">Trafalgar</p>
        </div>
        <p class="md:w-[330px] opacity-90 mt-5">{{data.text}}</p>
        <p class="opacity-90 mt-10">{{data.copy}}</p>
      </div>
      <div class="box2 mt-9 md:mt-0">
        <p class="font-semibold mb-5">Company</p>
        <p class="opacity-90 mb-2 cursor-pointer" v-for="i in data.company" :key="i">{{i}}</p>
      </div>
      <div class="box3 mt-9 md:mt-0">
        <p class="font-semibold mb-5">Region</p>
        <p class="opacity-90 mb-2 cursor-pointer" v-for="i in data.region" :key="i">{{i}}</p>
      </div>
      <div class="box4 mt-9 md:mt-0">
        <p class="font-semibold mb-5">Help</p>
        <p class="opacity-90 mb-2 cursor-pointer" v-for="i in data.help" :key="i">{{i}}</p>
      </div>
    </div>
    <img src="../../../assets/element.png" class="absolute -top-16 right-32 -z-10">
  </footer>
</template>

<script>
    import footerDataVue from '@/components/data/footerData.vue';

    export default {
        data() {
            return {
                data: footerDataVue.data()
            }
        }
    }
</script>

<style>
footer,
.footer-box {
  background: linear-gradient(183.41deg, #67c3f3 -8.57%, #5a98f2 82.96%);
}
</style>
