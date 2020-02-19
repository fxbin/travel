<template>
  <div class="home">
    <home-header/>
    <home-swiper/>
    <home-icons/>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeHeader from "@/components/home/Header";
import HomeSwiper from "@/components/home/Swiper";
import HomeIcons from "@/components/home/Icons";

export default {
  name: 'Home',
  components: {
    HomeIcons,
    HomeSwiper,
    HomeHeader
  }
}
</script>
