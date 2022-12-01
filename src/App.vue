<template>
  <div>
    <topMenu/>
    <mainContainer/>
    <pageFooter/>
  </div>
</template>

<script>
import './assets/tailwind.css'
import topMenu from './components/sections/header/topMenu.vue'
import mainContainer from './components/sections/main/main.vue'
import pageFooter from './components/sections/footer/pageFooter.vue'

export default {
  name: 'App',

  components: {
    topMenu,
    mainContainer,
    pageFooter,
  },

  data: () => ({
    
  }),
};
</script>
