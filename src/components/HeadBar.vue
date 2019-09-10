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
              T-Star挑战赛
            </router-link>
            <router-link to="/WXYun">
              云开发竞技赛
            </router-link>
          </div>
        </div>
      </nav>
    </header>
</template>

<script>
export default {
  data(){
    return {
      show:true
    }
  },
  mounted () {
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
header{
  position: fixed;
  background: rgba(59, 172, 227, 0.1);
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
</style>