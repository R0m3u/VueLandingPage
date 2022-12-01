<template>
    <div
      class="card w-[280px]  rounded-[20px] mb-24 md:mb-0" 
    >
      <div class="image-container h-[150px] w-full">
        <img :src="image" />
      </div>
      <div class="text px-5 py-5 ">
        <h3 class="text-xl font-bold mb-3">{{ title }}</h3>
        <p class="text-[#7D7987] text-base"> {{ text }} </p>
        <div class="relative max-w-[90px] mt-5 transition-all hover:animate-bounce">
            <a href="#" class="flex items-center h-max font-semibold text-[#4089ED]">
                Read more
                <img src="../../../assets/readMoreVector.png"  class="absolute top-[3.1px] bottom-0 left-[90px] my-auto" alt="">
            </a>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        props: ['image', 'title', 'text']
    }
</script>

<style scoped>
    .image-container img {
        width: 100%;
        height: 100%;
        border-top-left-radius: 20px;
        border-top-right-radius: 20px;
    }

    .card {
        box-shadow: 10px 40px 50px rgba(229, 233, 246, 0.4);
        background-color: #fff;
    }
</style>