<template>
  <section class="carousel relative md:h-[375px] w-auto px-6 relative">
    <img src="../../../assets/carouselAsset2.png" class="absolute bottom-24 left-[140px] hidden md:block">
    <div class="carousel-container max-w-[978px] md:h-[325px] rounded-3xl relative">
      <img src="../../../assets/carouselAsset.png" class="hidden md:block absolute -top-4 -right-5 hidden md:block">
      <h3 class="text-white text-center text-4xl font-semibold py-6 px-3 md:px-0">
        What our customer are saying
      </h3>
      <div class="testimonial">
        <div
          class="person mt-16 md:px-24 md:flex justify-around items-center transition-all animation-bounce"
          v-if="userInfo"
        >
          <div class="img flex flex-col md:flex-row items-center">
            <div class="mr-5 w-max border-4 border-white rounded-full mb-5 md:mb-0">
              <img
                class="rounded-full h-[100px] w-[100px]"
                :src="image"
                alt=""
              />
            </div>
            <div>
              <p class="name mb-1 text-xl text-white font-semibold">
                {{ userName }}
              </p>
              <p class="opacity-80 carrer text-white font-normal text-sm">
                {{ carrer }}
              </p>
            </div>
          </div>
          <div>
            <p
              class="leading-8 opacity-80 text-white w-auto max-w-[200px] md:max-w-[360px] mx-auto py-8 md:py-0"
            >
              ❝ {{ message }} ❞
            </p>
          </div>
        </div>
      </div>
      <div
        class="arrows absolute -bottom-14  flex items-center left-0 right-0 justify-around max-w-[350px] mx-auto"
      >
        <img
          class="arrow-left rotate-180"
          src="../../../assets/arrow.png"
          alt=""
          @click="user"
        />
        <div class="flex">
          <div
            v-for="user in users"
          
            :key="user"

            class="indicator opacity-30 firstD rounded-full w-2.5 h-2.5 bg-[#5B9BF3] transition-all" :class="{'selected': firstIndicator}"
          ></div>
        </div>
        <img
          class="arrow-right"
          src="../../../assets/arrow.png"
          alt=""
          @click="user"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      link: "",
      userName: "",
      carrer: "",
      message: "",
      id: 0,
      image: "",
      userInfo: "",
      users: 4

    };
  },
  mounted() {
    fetch(`https://testimonialapi.toolcarton.com/api`)
      .then((res) => res.json())
      .then((data) => {
        this.userInfo = data;
        this.userName = this.userInfo[this.id].name;
        this.carrer = this.userInfo[this.id].designation;
        this.image = this.userInfo[this.id].avatar;
        this.message = this.userInfo[this.id].message;
        // console.log(this.userInfo);
      })
      .catch((err) => console.log(err));
  },

  methods: {
    user() {
      this.id += 1;
      this.userName = this.userInfo[this.id].name;
      this.carrer = this.userInfo[this.id].designation;
      this.image = this.userInfo[this.id].avatar;
      this.message = this.userInfo[this.id].message;
      this.fade();
      // console.log(performance.now());

      const dots = document.querySelectorAll('.indicator');
      const first = document.querySelectorAll('.indicator:first-child');
      
      console.log(first)
      
      

      dots.forEach((dot,i) => {
        if(i === 0) dot.classList.add('selected');
        dot.classList.remove('selected');
        dots[this.id].classList.add('selected');
      });

      if (this.id > 2) {
        this.id = -1;
      }
      return this.id;
    },

    fade() {
      const person = document.querySelector(".person");
      person.classList.add("fade");
      setTimeout(() => {
        person.classList.remove("fade");
      }, 800);
    },
  },
  computed: {
    firstIndicator() {
      if(this.id === 0) {
        return {
          opacity: 1
        }
      }

      return this.id;
    }
  }
};
</script>

<style scoped>
.carousel-container {
  background: linear-gradient(208.18deg, #67c3f3 9.05%, #5a98f2 76.74%);
  margin: 4rem auto 10rem auto;
}

div h3 {
  position: relative;
}

div h3:after {
  position: absolute;
  content: "";
  width: 40px;
  height: 3px;
  background-color: #fff;
  bottom: 0;
  left: 0;
  right: 0;
  margin: 0 auto;
  opacity: 0.7;
}

.arrow-left,
.arrow-right {
  cursor: pointer;
}
.indicator {
  margin-right: 18px;
}


.indicator:last-child {
  margin: 0;
}

.selected {
  opacity: 1;
}

.fade {
  animation: fadein 1s;
}

@keyframes fadein {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}
</style>
>
