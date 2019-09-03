<template>
  <div class="home">
    <ClubIntroduce/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import ClubIntroduce from '@/components/ClubIntroduce.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'home',
  components: {
    ClubIntroduce,
    Footer
  }
}
</script>
