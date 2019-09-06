<template>
  <div class="home">
    <ClubIntroduce/>
    <br/>
    <ClubApartmentIntroduce :showTitle="true"/>
    <br/><br/>
    <Footer/>
  </div>
</template>

<script>
  // @ is an alias to /src
  import ClubIntroduce from '@/components/ClubIntroduce.vue'
  import ClubApartmentIntroduce from '@/components/ClubApartmentIntroduce.vue'
  import Footer from '@/components/Footer.vue'

  export default {
    name: 'Home',
    components: {
      ClubIntroduce,
      ClubApartmentIntroduce,
      Footer
    }
  }
</script>

<style scoped>
  .home {
    background-image: url('../assets/low-poly-bg.jpg');
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-attachment: fixed;
    text-align: center;
  } 
</style>
