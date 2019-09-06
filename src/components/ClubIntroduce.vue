<template>
  <div class="club-introduce">
    <img alt="XDTIC logo" src="../assets/logo.png" style="margin-top: 60px">
    <h1>欢迎访问西电腾讯创新俱乐部</h1>
    <div class="data-list">
      <div class="data-item" v-for="(d, index) in clubData" :key="index">
        <div class="data-top">
          <div class="data-num">
            {{d.num}}
          </div>
          <div class="data-unit">
            {{d.unit}}
          </div>
        </div>
        <div class="data-bottom">
          {{d.bottom}}
        </div>
      </div>
    </div>
    <Row>
      <Col span="4">
        &nbsp;
      </Col>
      <Col span="16">
        <h3>什么是腾讯创新俱乐部？</h3>
        <div class="text-block">
          为加强和促进腾讯与高校在科研技术、人才培养以及校园活动等方面的合作，腾讯已陆续在全国21所高校内建立了腾讯创新俱乐部。
          俱乐部以“互联网技术和产品”为核心定位，提倡自由、开放、分享的文化氛围，旨在为高校学生打造一个学习、创新以及应用互联网技术、提升展示自我的平台，
          让学生在互联网技术学习和产品创新过程中，充分参与项目管理、产品设计、用户需求和体验、产品技术开发实现、产品运营和服务等实践活动，从而全面提升学生的专业能力和综合素质。
        </div>
        <h3>俱乐部活动瞬间</h3>
        <Carousel autoplay loop :autoplay-speed="5000" v-model="carouseValue" easing="ease">
          <CarouselItem>
            <img alt="carouse_home_1.jpg" src="../assets/carouse_home_1.jpg"/>
          </CarouselItem>
          <CarouselItem>
            <img alt="carouse_home_2.jpg" src="../assets/carouse_home_2.jpg"/>
          </CarouselItem>
          <CarouselItem>
            <img alt="carouse_home_3.jpg" src="../assets/carouse_home_3.jpg"/>
          </CarouselItem>
          <CarouselItem>
            <img alt="carouse_home_4.jpg" src="../assets/carouse_home_4.jpg"/>
          </CarouselItem>
        </Carousel>
      </Col>
      <Col span="4">
        &nbsp;
      </Col>
    </Row>
  </div>
</template>

<script>
  import {Row, Col, Carousel, CarouselItem} from 'iview';
  import Header from '@/components/headbar.vue';

  export default {
    name: 'ClubIntroduce',
    props: {
      msg: String
    },
    data() {
      return {
        carouseValue: 2,
        clubData: [
          {
            'num': 4,
            'unit': '个',
            'bottom': '主要部门',
          },
          {
            'num': '100+',
            'unit': '名',
            'bottom': '现任成员',
          },
          {
            'num': '30+',
            'unit': '项',
            'bottom': '各类奖项',
          },
          {
            'num': new Date().getFullYear() - 2007, // 2007 年建立
            'unit': '年',
            'bottom': '创建历史',
          }
        ]
      }
    },
    components: {
      Row,
      Col,
      Carousel,
      CarouselItem,
      Header
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .text-block {
    font-size: 1.28571429rem;
    text-align: center;
    line-height: 2.35714286rem;
  }

  h1 {
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

  .data-list {
    display: flex;
    margin: 55px 150px;
    justify-content: space-between;
  }

  .data-list .data-item {
    text-align: center;
  }

  .data-list .data-item .data-top {
    text-align: center;
    display: flex;
    justify-content: center;
    padding-bottom: 8px;
    border-bottom: 1px solid #ddd;
    min-width: 280px;
  }

  .data-list .data-item .data-top .data-num {
    color: #3bace3;
    font-weight: 700;
    margin-right: 8px;
    font-size: 4rem;
  }

  .data-list .data-item .data-top .data-unit {
    padding-top: 3rem;
    font-size: 1.2rem;
    line-height: 1;
    color: rgba(0, 0, 0, .3);
    width: inherit;
  }

  .data-list .data-item .data-bottom {
    color: #414141;
    font-size: 1rem;
    line-height: 1.2;
    margin-top: 10px;
  }
</style>
