<template>
    <header v-if="show">
      <nav id="headbar">
        <div class="head-container">
          <div class="head-brand">
          <h1 style="margin:0">TC Club</h1>
          </div>
          <div class="head-links">
            <router-link to="/">
              HOME
            </router-link>
            <router-link to="/about">
              ABOUT
            </router-link>
          </div>
        </div>
      </nav>
    </header>
</template>

<<script>
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
      var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
      if(scrollTop > 100){
        this.show = false;
      } else {
        this.show = true;
      }
    }
  },
}
</script>

<style scoped>
header{
  position: fixed;
  background: rgba(245, 245, 245, 0.3);
  width: 100%;
}
#headbar {
  height: 8vh;
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