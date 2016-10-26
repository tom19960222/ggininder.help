<template>
  <div>
    <div><a v-bind:href="galleryLink"><img class="image-block" v-bind:src="galleryURL" /></a></div>
    <p>{{ galleryName }}</p>
    <button class="re-random-button" @click="reRandom">{{ reRandomButtonMessage }}</button>
  </div>
</template>

<script>
  export default {
    name: 'RandomGallery',
    data () {
      return {
        galleryURL: 'http://i.imgur.com/xVeMPLH.jpg',
        galleryLink: 'http://g.e-hentai.org/g/774929/35cbb9a870/',
        galleryName: '(C87) [比村乳業 (比村奇石)] 魔性の潮 (艦隊これくしょん -艦これ-)',
        reRandomButtonMessage: '重新硬硬',
        galleryLinkList: [
          {
            galleryURL: 'http://i.imgur.com/xVeMPLH.jpg',
            galleryLink: 'http://g.e-hentai.org/g/774929/35cbb9a870/',
            galleryName: '(C87) [比村乳業 (比村奇石)] 魔性の潮 (艦隊これくしょん -艦これ-)'
          },
          {
            galleryURL: 'http://i.imgur.com/m19khJU.jpg',
            galleryLink: 'http://g.e-hentai.org/g/843016/5f68592043/',
            galleryName: '(C88) [比村乳業 (比村奇石)] 続・魔性の潮 (艦隊これくしょん -艦これ-)'
          },
          {
            galleryURL: 'http://i.imgur.com/ReZawHQ.jpg',
            galleryLink: 'http://g.e-hentai.org/g/843689/68834bcc2a/',
            galleryName: '(C88) [比村乳業 (比村奇石)] 魔性の潮+α (艦隊これくしょん -艦これ-)'
          }
        ]
      }
    },
    methods: {
      reRandom: function () {
        var index = Math.floor(Math.random() * this.galleryLinkList.length)
        this.galleryURL = this.galleryLinkList[index].galleryURL
        this.galleryLink = this.galleryLinkList[index].galleryLink
        this.galleryName = this.galleryLinkList[index].galleryName1
      }
    }
  }
</script>

<style scoped>
    .re-random-button{
        width: 200px;
        height: 50px;
        font-size: 25px;
    }
    .image-block{
        width: 350px;
        height: auto;
    }
</style>