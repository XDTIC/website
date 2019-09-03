<template>
  <div class="root">
    <Row>
      <Col span="6">
        &nbsp;
      </Col>
      <Col span="12">
        <div class="ft-left">
          <img alt="gzh-qcode.png" src="../assets/gzh-qcode.png" width="120"/>
        </div>
        <div class="ft-right">
          <p>
            友情链接
          </p>
          <div class="link-a">
            <a href="https://ur.tencent.com/" target="_blank" rel="noopener">
              <img alt="ur-logo.png" src="../assets/ur-logo.png" width="145px"/>
            </a>
            <a href="https://weixiao.qq.com/" target="_blank" rel="noopener">
              <img alt="weixiao-logo.png" src="../assets/weixiao-logo.png" width="145px"/>
            </a>
          </div>
        </div>
      </Col>
      <Col span="6">
        &nbsp;
      </Col>
    </Row>
  </div>
</template>

<script>
  import {Row, Col} from 'iview'
  export default {
    name: "Footer",
    components:{
      Row,
      Col
    }
  }
</script>

<style scoped>
  .root {
    background: #2a2f35;
    min-height: 200px;
  }
  .ft-left {
    display: inline-block;
    vertical-align: middle;
    width: 330px;
    padding: 0 15px;
  }
  .ft-right {
    display: inline-block;
    vertical-align: middle;
    border-left: 1px solid #646f7c;
    width: 400px;
    min-height: 150px;
    margin: 20px;
  }
  .ft-right p{
    font-size: 1rem;
    border-bottom: 3px solid #4680fe;
    color: white;
    width: 100px;
    margin-left: 50px
  }
  .link-a a {
    display: inline-block;
    margin: 35px 10px;
  }
</style>