<template>
  <header>
    <nav
      class="
        h-[100px]
        flex
        justify-between
        md:justify-around
        items-center
        md:px-0
        max-w-7xl
        m-auto
      "
    >
      <div class="cursor-pointer logo flex items-center">
        <p
          class="
            m-[12px]
            font-semibold
            bg-sky-600
            h-10
            w-10
            text-white text-2xl text-center
            leading-[2.5rem]
            rounded-full
            align-center
          "
        >
          T
        </p>
        <p class="text-2xl font-bold">Trafalgar</p>
      </div>
      <div
        @click="open = !open"
        class="
          mr-[34px]
          h-[100px]
          flex flex-col
          items-center
          justify-center
          md:hidden
          z-10
        "
        :class="[{ relative: !open }, { absolute: open }, { 'right-0': open }]"
      >
        <div
          class="absolute w-[30px] h-1 bg-black transition-all rounded"
          :class="[{ 'rotate-45': open }, { 'top-9': !open }, {'bg-white': open}]"
        ></div>
        <div
          class="absolute w-[30px] h-1 bg-black transition-all rounded"
          :class="{ 'opacity-0': open }"
        ></div>
        <div
          class="absolute w-[30px] h-1 bg-black transition-all rounded"
          :class="[{ '-rotate-45': open }, { 'bottom-9': !open }, {'bg-white': open}]"
        ></div>
      </div>
      <div
        class="
          menu
          flex flex-col
          justify-center
          fixed
          top-0
          right-0
          h-screen
          w-[200px]
          bg-[#458FF6]
          text-white
          rounded-tl-2xl
          transition-all
          md:relative md:h-max md:w-max md:bg-transparent md:text-black md:translate-x-0
        "
        :class="{'translate-x-full': !open}"
      >
        <ul
          class="
            relative
            bottom-24
            justify-around justify-around
            transition
            md:flex md:text-black md:flex-row md:bottom-0
          "
          :class="{}"
        >
          <li
            class="text-lg mx-[20px] lg:mx-[30px] cursor-pointer mb-3 md:mb-0"
            v-for="item in menuItems"
            :key="item"
          >
            {{ item }}
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      menuItems: ["Home", "Find a doctor", "Apps", "Testimonials", "About us"],
      open: false,
    };
  },
};
</script>

<style>
/*fazer o menu lateral responsivo mobile*/
</style>