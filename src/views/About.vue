<template>
  <div class="about">
    <!-- <div class="backBtn">
      <router-link to="/" style="color: white">返回首页</router-link>
    </div> -->
    <Row style="width: 75%;margin:auto">
      <Col span="16">
        <Card style="width:320px" v-for="(d, index) in developer" :key="index">
          <div style="text-align:center;opacity:0.9">
            <img :alt="d.avatar" :src="d.avatar" width="250"/>
            <h3 style="margin: 10px">{{d.id}}</h3>
            <p style="margin: 10px">{{d.bio}}</p>
            <a :href="d.github" target="_blank" rel="noopener">{{d.id}}</a>@Github
          </div>
        </Card>
      </Col>
    </Row>
  </div>
</template>
<script>
  import {Row, Col, Card} from 'iview';
  import whiterobeAvatar from '../assets/whiterobe-avatar.png';
  import Header from '@/components/headbar.vue'

  export default {
    name: 'Home',
    data() {
      return {
        developer: [
          {
            avatar: whiterobeAvatar,
            id: 'WhiteRobe',
            bio: 'Learning. Sharing.',
            github: 'https://github.com/WhiteRobe'
          }
        ]
      }

    },
    components: {
      Row,
      Col,
      Card,
      Header
    }
  }
</script>

<style scoped>
  .about {
    /* background-image: url('../assets/Star-Emission0.png'); */
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-attachment: fixed;
    /* height: 960px; */
    min-height: 100vh;
    text-align: center;
  }

  div {
    font-size: 1rem;
  }

  .backBtn {
    line-height: 3rem;
    background: rgba(0, 153, 229, .7);
    color: #fff;
    text-align: center;
    bottom: 0;
    position: fixed;
    width: 100%;
  }
</style>
