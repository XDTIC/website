<template>
  <div class="club-apartment-introduce">
    <Row>
      <Col span="5" style="display: flex; justify-content: center">
        <div class="left">
          <span @mouseenter="onEnter('tech')"><Icon type="md-construct" />&nbsp;技术部</span>
          <span @mouseenter="onEnter('alg')"><Icon type="ios-flask" />&nbsp;算法部</span>
        </div>
      </Col>
      <Col span="14">
        <h3 v-if="showTitle">各部门简介</h3>
        <div class="middle">
          <div class="middle-wrap">
            <span v-html="info"></span>
          </div>
        </div>
      </Col>
      <Col span="5" style="display: flex; justify-content: center">
        <div class="right">
          <span @mouseenter="onEnter('product')"><Icon type="md-cube"/>&nbsp;产品部</span>
          <span @mouseenter="onEnter('maintain')"><Icon type="md-contacts"/>&nbsp;运营部</span>
        </div>
      </Col>
    </Row>
  </div>
</template>

<script>
  import {Row, Col, Icon} from 'iview'
  import apartmentIntroduce from '../assets/apartmentIntroduce.json';

  export default {
    name: "ClubApartmentIntroduce",
    props: {
      showTitle: Boolean
    },
    mounted() {
      this.info = this.infoList['tech']; // 默认显示技术部的简介
    },
    data() {
      return {
        info: '显示信息',
        infoList: apartmentIntroduce
      }
    },
    methods: {
      onEnter(tag) {
        this.info = this.infoList[tag]
      }
    },
    components: {
      Row,
      Col,
      Icon
    }
  }
</script>

<style scoped>
  .club-apartment-introduce {
  }

  h3 {
    font-size: 1.58571429rem;
    margin: 20px 0;
  }


  .left, .right {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-width: 175px;
    max-width: 175px;
    height: 500px;
    margin-top: 75px;
    padding: 75px 0;
  }

  .middle {
    height: 500px;
    padding: 0 25px;
    border-left: 5px solid #ddd;
    border-right: 5px solid #ddd;
  }

  .middle .middle-wrap {
    text-align: left;
    font-size: 1rem;
    line-height: 1.5rem;
    padding: 50px 20px;
    background: white;
    border-radius: 20px;
    height: 100%;
    border: 1px solid rgba(0, 0, 0, .1);
  }


  @keyframes swing {
    from {
      transform: translate(0, 0)
    }
    to {
      transform: translate(0, 16px)
    }
  }

  @-webkit-keyframes swing {
    from {
      transform: translate(0, 0)
    }
    to {
      transform: translate(0, 16px)
    }
  }

  .left span, .right span {
    background: #3bace3;
    width: inherit;
    height: 75px;
    border-radius: 25px;
    font-size: 1.5rem;
    color: white;
    font-weight: 500;
    /*文字垂直居中*/
    display: flex;
    justify-content: center;
    align-items: center;
    /*上下浮动的动画*/
    animation: swing 1.3s ease-in-out 2.7s infinite alternate;
    -webkit-animation: swing 1.3s ease-in-out 2.7s infinite alternate;
  }
</style>