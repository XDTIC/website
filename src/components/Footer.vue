<template>
  <div class="footer">
    <Row>
      <Col span="2">
        &nbsp;
      </Col>
      <Col span="20">
        <div class="ft-left">
          <img alt="gzh-qcode.png" src="../assets/gzh-qcode.png" width="120"/>
          <p>扫一扫，了解俱乐部动态</p>
        </div>
        <div class="ft-right">
          <p>
            友情链接
          </p>
          <div class="link-a">
            <a href="https://ur.tencent.com" target="_blank" rel="noopener">
              <img alt="ur-logo.png" src="../assets/ur-logo.png"/>
            </a>
            <a href="https://weixiao.qq.com" target="_blank" rel="noopener">
              <img alt="weixiao-logo.png" src="../assets/weixiao-logo.png"/>
            </a>
            <a href="https://www.xidian.edu.cn" target="_blank" rel="noopener">
              <img alt="xd-logo.png" src="../assets/xd-logo.png"/>
            </a>
          </div>
        </div>
      </Col>
      <Col span="2">
        &nbsp;
      </Col>
    </Row>
    <div class="copyright">
      Copyright © 2019 Tencent Innovation Club, Xidian University. All Rights Reserved.
    </div>
    <div class="introduce">
      腾讯创新俱乐部的官网还在开发中，请访问
      <a href="https://github.com/WhiteRobe/xdtic-web" target="_blank" rel="noopener">xdtic-web@Github</a>了解或加入开发 |
      <router-link to="/about"> 关于页面开发者 </router-link>
    </div>
    <div class="introduce" style="color: lightblue; opacity: 0.6;">
      <span id="busuanzi_container_site_pv" style="display: none">
          总访问量<span id="busuanzi_value_site_pv"></span>次 |
      </span>
      <span>
        本站已运行:{{Math.floor((new Date()-new Date('2019-09-01')) / 1000 / 3600 / 24)}}天
      </span>
    </div>
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
  .footer {
    background: #2a2f35;
    min-height: 200px;
  }
  .ft-left {
    display: inline-block;
    vertical-align: middle;
    width: 330px;
    padding: 0 15px;
  }
  .ft-left p {
    color: whitesmoke;
  }
  .ft-right {
    display: inline-block;
    vertical-align: middle;
    border-left: 1px solid #646f7c;
    min-height: 150px;
    margin: 20px;
  }
  .ft-right img{
    max-width: 200px;
    max-height: 80px;
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
  .copyright {
    color: snow;;
    text-align: center;
    font-size: .9rem;
    line-height: 1.5rem;
  }
  .introduce {
     color: gray;
     text-align: center;
     font-size: .75rem;
     line-height: 1.5rem;
   }
</style>