<template>
  <div class="home">
    <home-header/>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeHeader from '@/components/home/Header.vue'

export default {
  name: 'Home',
  components: {
    HomeHeader
  }
}
</script>
