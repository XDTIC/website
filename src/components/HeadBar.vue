<template>
  <header v-if="show">
    <nav class="head-bar">
      <div class="head-container">
        <div class="head-brand">
          <h1 style="margin:0;color: black;">
            <router-link to="/">
              XDTIC主页
            </router-link>
          </h1>
        </div>
        <div class="head-links">
          <router-link to="/TStar">
            <div  class="btn animated infinite tada slower delay-3s">T-Star挑战赛</div >
          </router-link>
          <router-link to="/WXYun">
            <div  class="btn animated infinite tada slower delay-3s">云开发竞技赛</div >
          </router-link>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
  export default {
    data() {
      return {
        show: true
      }
    },
    mounted() {
      window.addEventListener('scroll', this.scrollToTop)
    },
    methods: {
      scrollToTop() { // 监听滚动条，动态隐藏标题栏
        let scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
        this.show = scrollTop <= 100
      }
    },
  }
</script>

<style scoped>
  header {
    position: fixed;
    background: rgba(206, 201, 196, 0.3);
    width: 100%;
    z-index: 999;
  }

  .head-bar {
    height: 75px;
  }

  .head-container {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 75%;
    margin: 0 auto;
  }

  .head-links a {
    padding: 10px 10px;
    color: black;
    font-size: 1.5rem;
    text-decoration-line: none;
  }

  .head-links .btn{
    background: rgba(59, 172, 227, 0.8);
    padding: 10px 15px;
    border-radius: 15px;
    color: white;
    display: inline-block;
    font-size: 1.2rem;
    margin: 0 30px;
  }
</style>