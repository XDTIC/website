<template>
  <div class="root">
    <img alt="XDTIC logo" src="../assets/logo.png" style="margin-top: 60px">
    <h1>欢迎访问西电腾讯创新俱乐部</h1>
    <div class="introduce-subline">
      腾讯创新俱乐部的官网还在开发中，请访问
      <a href="https://github.com/WhiteRobe/xdtic-web" target="_blank" rel="noopener">xdtic-web@Github</a>了解或加入开发。
    </div>
    <Row>
      <Col span="6">
        &nbsp;
      </Col>
      <Col span="12">
        <h3>什么是腾讯创新俱乐部？</h3>
        <div class="text-block">
          为加强和促进腾讯与高校在科研技术、人才培养以及校园活动等方面的合作，腾讯已陆续在全国21所高校内建立了腾讯创新俱乐部。
          俱乐部以“互联网技术和产品”为核心定位，提倡自由、开放、分享的文化氛围，旨在为高校学生打造一个学习、创新以及应用互联网技术、提升展示自我的平台，
          让学生在互联网技术学习和产品创新过程中，充分参与项目管理、产品设计、用户需求和体验、产品技术开发实现、产品运营和服务等实践活动，从而全面提升学生的专业能力和综合素质。
        </div>
        <h3>俱乐部活动瞬间</h3>
        <Carousel autoplay loop autoplay-speed="3000" v-model="carouseValue" easing="ease">
          <CarouselItem>
            <img alt="carouse_home_1.jpg" src="../assets/carouse_home_1.jpg" />
          </CarouselItem>
          <CarouselItem>
            <img alt="carouse_home_2.jpg" src="../assets/carouse_home_2.jpg" />
          </CarouselItem>
          <CarouselItem>
            <img alt="carouse_home_2.jpg" src="../assets/carouse_home_3.jpg" />
          </CarouselItem>
          <CarouselItem>
            <img alt="carouse_home_3.jpg" src="../assets/carouse_home_4.jpg" />
          </CarouselItem>
        </Carousel>
        <h3>加入俱乐部</h3>
        <div class="text-block" style="text-align: center">
          开发中........
        </div>
      </Col>
      <Col span="6">
        &nbsp;
      </Col>
    </Row>

    <br/>
    <br/>
  </div>
</template>

<script>
  import {Row, Col, Carousel, CarouselItem} from 'iview'

  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    },
    data() {
      return {
        carouseValue: 0,
        carouseImgs: [
          "carouse_home_1.jpg",
          "carouse_home_2.jpeg",
          "carouse_home_3.jpg",
          "carouse_home_4.jpg"
        ]
      }
    },
    components: {
      Row,
      Col,
      Carousel,
      CarouselItem
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .root{
    background-image:url('../assets/low-poly-bg.jpg');
    background-repeat:no-repeat;
    background-size:100% 100%;
    background-attachment:fixed;
  }

  .introduce-subline {
    text-align: center;
    font-size: 1rem;
    line-height: 2.35714286rem;
  }

  .text-block {
    font-size: 1.28571429rem;
    text-align: center;
    line-height: 2.35714286rem;
  }

  h1{
    font-size: 1.68571429rem;
    margin: 40px 0 10px;
  }

  h3 {
    font-size: 1.58571429rem;
    margin: 20px 0;
  }

  a {
    color: #00b0fb;
  }
</style>
