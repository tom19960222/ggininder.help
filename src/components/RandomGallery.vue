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
          },
          {
            galleryURL: 'http://i.imgur.com/FiBPxlz.jpg',
            galleryLink: 'http://g.e-hentai.org/g/730137/b882d40aaa/',
            galleryName: '(C86) [天堂紙 (天堂樹)] あなたの世界へ (艦隊これくしょん -艦これ-)'
          },
          {
            galleryURL: 'http://i.imgur.com/XGFLy37.jpg',
            galleryLink: 'http://g.e-hentai.org/g/974818/e2306757a1/',
            galleryName: '(COMIC1☆9) [天堂紙 (天堂樹)] 貴女の守り方'
          },
          {
            galleryURL: 'http://i.imgur.com/TTALL3o.jpg',
            galleryLink: 'http://g.e-hentai.org/g/990175/ab2a51ef12/',
            galleryName: '(みみけっと35) [RIKOMAM (梱枝りこ、蜜桃まむ)] りこまむ★PYON (ご注文はうさぎですか?)'
          },
          {
            galleryURL: 'http://i.imgur.com/j67D3xu.jpg',
            galleryLink: 'http://g.e-hentai.org/g/941310/e73ae58c9f/',
            galleryName: '(C89) [こつぶあん (凍奈)] うさ耳ハプニング!! リターンズ (ご注文はうさぎですか？)'
          },
          {
            galleryURL: 'http://i.imgur.com/2sw1poj.jpg',
            galleryLink: 'http://g.e-hentai.org/g/903416/5c1da7de0a/',
            galleryName: '(C89) [eterna-radiare (りいちゅ)] Fluffy (ご注文はうさぎですか?)'
          },
          {
            galleryURL: 'http://i.imgur.com/PzrQ3nA.jpg',
            galleryLink: 'http://g.e-hentai.org/g/900223/7c6c370cfe/',
            galleryName: '(C89) [無人少女 (梱枝りこ)] COCO CHINO 2 (ご注文はうさぎですか?)'
          }
        ]
      }
    },
    methods: {
      reRandom () {
        var index = Math.floor(Math.random() * this.galleryLinkList.length)
        this.galleryURL = this.galleryLinkList[index].galleryURL
        this.galleryLink = this.galleryLinkList[index].galleryLink
        this.galleryName = this.galleryLinkList[index].galleryName
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