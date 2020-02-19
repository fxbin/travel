<template>
  <div class="home">
    <home-header/>
    <home-swiper/>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeHeader from '@/components/home/Header.vue'
import HomeSwiper from "@/components/home/Swiper";

export default {
  name: 'Home',
  components: {
    HomeSwiper,
    HomeHeader
  }
}
</script>
