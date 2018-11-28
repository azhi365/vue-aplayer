<template>
  <div id="app">
    <div class="container">
      <aplayer
        autoplay
        theme="pic"
        shuffle
        repeat="list"
        show-lrc
        :muted.sync="muted"
        :volume.sync="volume"
        :music='list3[0]'
        :list='list3'
      />
    </div>
  </div>
</template>
<script>
  import Aplayer from '../vue-aplayer.vue'

  export default {
    name: 'App',
    components: {
      Aplayer,
    },
    data () {
      return {
        version: VERSION,
        volume: 1,
        muted: false,
        music3: null,
        list3: [
          {
            title: '前前前世',
            artist: 'RADWIMPS',
            src: 'http://s1.innstack.com//audio/382/14654.mp3',
            pic: 'http://192.168.1.166:3000/aplayer/yourname.jpg',
            lrc: '',
          },
          {
            title: '光るなら.m3u8',
            artist: 'Goose house',
            src: 'http://s1.innstack.com//audio/382/14655.mp3',
            pic: 'http://192.168.1.166:3000/aplayer/hikarunara.jpg',
            lrc: '',
          },
          {
            title: '回レ！雪月花',
            artist: '小倉唯',
            src: 'http://s1.innstack.com//audio/382/14656.mp3',
            pic: 'http://192.168.1.166:3000/aplayer/snowmoonflowers.jpg',
            lrc: '',
          },
          {
            title: 'あっちゅ～ま青春!',
            artist: '七森中☆ごらく部',
            src: 'http://s1.innstack.com//audio/382/14657.mp3',
            pic: 'http://192.168.1.166:3000/aplayer/yuruyuri.jpg',
            lrc: '',
          },
        ],
      }
    }
  }
</script>
<style>
  html, body {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
    overflow: hidden;
  }

  body {
    font-family: Source Sans Pro, 'PingFang SC', 'Helvetica Neue', Helvetica, Arial, sans-serif;
    background: linear-gradient(135deg, rgb(65, 184, 131), rgb(74, 156, 238));
    color: #fff;
    overflow-y: auto;
  }

  #app {
    text-align: center;
  }

  .container {
    max-width: 64rem;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 50px;
    bottom: 0rem;

  }

  h1 {
    font-size: 48px;
    margin: 30px 0 10px;
  }

  h3 {
    font-size: 24px;
  }

  input {
    background-color: transparent;
    outline: none;
    border: none;
    color: inherit;
    font-size: inherit;
    text-align: center;
    border-bottom: 1px solid rgba(255, 255, 255, .5);
  }

  a {
    color: #35495e;
    text-decoration: none;
  }

  p {
    font-size: 18px;
  }
</style>