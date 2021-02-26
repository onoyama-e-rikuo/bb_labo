<template>
  <div>
    <div id="a" class="text-h5 font-weight-medium mt-8">{{ name }}</div>
    <div class="text-caption font-weight-medium">
      {{ title }} / {{ subTitle }}
    </div>
    <v-img :src="pic"
           class="mt-8"></v-img>
    <div class="text-body-1 font-weight-medium mt-8">メッセージ</div>
    <p class="text-body-2 mt-4">
      {{ message }}
    </p>
    <v-row no-gutters justify="space-around">
        <v-col v-for="interviewee in interviewees" :key="interviewee.id"
               cols="10" class="mt-8">
            <a href="#" v-scroll-to="{el: '#a', offset: -60}" class="a">
          <v-card
            class="d-flex"
            max-height="70px"
            @click="selected(interviewee.id)"
          >
            <div
              class="mini-profile d-flex align-start justify-center flex-column pl-2"
            >
              <div class="text-body-2 font-weight-bold">
                {{ interviewee.name }}
              </div>
              <div class="text-caption">{{ interviewee.title }}</div>
              <div class="text-caption">{{ interviewee.subTitle }}</div>
            </div>
            <v-img :src="interviewee.pic" max-width="50%"></v-img>
          </v-card>
            </a>
        </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import VueScrollTo from 'vue-scrollto'

@Component
export default class Messages extends Vue {
  private id = 1
  private name = '坪井 智哉'
  private title = '横浜DeNAベイスターズ'
  private subTitle = '一軍打撃コーチ'
  private message =
    '目標を達成するためには何が必要か？！独立リーグからプロ野球界に飛び込み、その厳しい世界で戦ってきた苦労人だからこそ解ることがあります。努力している皆様の為、彼は自分の事のように寄り添いサポートしてくれると思います。人情味あふれる男、西川雅人と『BB LABO.』をよろしくお願い致します。'
  private pic = require('../assets/images/interview/S__27918358.jpg')

  // private scroll() {
  //   window.scrollTo({
  //     top: this.$refs.name as any,
  //     behavior: "smooth"
  //   })
  // }

  private selected(id: number) {
    this.id = id
    this.name = this.interviewees[id].name
    this.title = this.interviewees[id].title
    this.subTitle = this.interviewees[id].subTitle
    this.message = this.interviewees[id].message
    this.pic = this.interviewees[id].pic
  }
  private interviewees = [
    {
      id: 0,
      name: '坪井 智哉',
      title: '横浜DeNAベイスターズ',
      subTitle: '一軍打撃コーチ',
      message:
        '目標を達成するためには何が必要か？！独立リーグからプロ野球界に飛び込み、その厳しい世界で戦ってきた苦労人だからこそ解ることがあります。努力している皆様の為、彼は自分の事のように寄り添いサポートしてくれると思います。人情味あふれる男、西川雅人と『BB LABO.』をよろしくお願い致します。',
      pic: require('../assets/images/interview/S__27918358.jpg'),
    },
    {
      id: 1,
      name: '吉岡 雄二',
      title: '富山サンダーバーズ',
      subTitle: '監督',
      message:
        '現役時代、彼には、何事にも素直に取り組むよう指導しました。プロ野球で学んだ技術から、メンタル的なことまで、より洗練させ、1人でも多くの人を幸せにしてくれると願っています。応援してるよ！！',
      pic: require('../assets/images/interview/S__27918360.jpg'),
    },
    {
      id: 2,
      name: '星野 おさむ',
      title: '福島レッドホープス',
      subTitle: 'GM兼総合コーチ',
      message:
        '現役時代の西川には「段取り十分( じゅうぶ ) 」そして「 慢心する事なく野球に向き合うように 」と語ってきました。強い信念と辛抱強さを持った男です。野球で学んだ経験を活かし指導者としても活躍してくれる事と信じています。',
      pic: require('../assets/images/interview/S__27918364.jpg'),
    },
    {
      id: 3,
      name: '萩原 淳',
      title: '滋賀ユナイテッド',
      subTitle: 'コーチ',
      message:
        'どんなメニューにも、歯を食いしばって頑張っていた姿を思い出します。私の指導は、決して妥協する事なく厳しいものでした。それにも耐えた彼だからこそ、最後まで全力でサポートできるはずです。たくさんの人の力になれるように頑張れ！！',
      pic: require('../assets/images/interview/S__27918366.jpg'),
    },
    {
      id: 4,
      name: '加藤 大輔',
      title: '元オリックス･バファローズ',
      subTitle: '',
      message:
        '入団発表の時に「 加藤さんに追いつく!! 」と豪語したことがきっかけで、可愛がった後輩が西川です。お互いに速球で押していくスタイルは同じでしたが、考え方やフォームなどは人それぞれ違います。もっといいパフォーマンスを出す、成績を安定させるためには、体の強さだけではなく、考え方や使い方が重要です。『BB LABO.』なら、その両方を鍛えることが出来ます！マンツーマン指導なので、自分に本当にあったフォーム作り、体力UPが出来ますよ！️プロ野球選手として身に付けたメソッドは、どんな方にも応用できると思いますので、まずは体験してみてください！',
      pic: require('../assets/images/interview/S__27918368.jpg'),
    },
    {
      id: 5,
      name: '高宮 和也',
      title: '元阪神タイガース',
      subTitle: '',
      message:
        'のりお ( 西川のあだ名で以下のりお ) とは、アマチュア時代の日本代表候補合宿で一緒でした。紆余曲折して、プロの世界に入ったのりおだからこその経験を活かす事が、目標を持つ人に対しての力に絶対になる!!気合いと根性やぞ!!最後に、これが一番大切な事ですが…皆さん♬僕のYouTubeも是非ご覧いただき、チャンネル登録よろしくお願いします。',
      pic: require('../assets/images/interview/S__27918370.jpg'),
    },
    {
      id: 6,
      name: '梶本 達哉',
      title: '元オリックス・バファローズ',
      subTitle: '',
      message:
        'まずはトレーニングジムの開設、誠におめでとうございます。\n' +
        '\n' +
        '僕も引退してから、一時期地元の子供達に野球の指導をしていた事があるので、その難しさや、やり甲斐は少し分かりますし、その大切さ、重要性はすごく感じてます。\n' +
        'ただ、そんな環境が中々みんなのところまで届けれないと思われている中、\n' +
        '\n' +
        '野球を元プロ選手に教えてもらえて、\n' +
        'さらにトレーニングもできるジムって、、、\n' +
        '最強ですやん。\n' +
        '\n' +
        '非常に素晴らしい取り組みだと思います。\n' +
        '僕もまた何かお手伝い出来る事あれば呼んでくださいw\n' +
        '\n' +
        '西川さんはもちろん大好きな先輩ですし、現役時代はとても長い時間を共にさせていただいた戦友のような関係でもあると、勝手ながら思わせてもらってます。\n' +
        'その戦友の先輩がまた新たな戦いするって？\n' +
        '応援しないわけないでしょ。\n' +
        '\n' +
        '決して脅されて書いてるわけでないですよ。決して。\n' +
        '\n' +
        'そんな、顔は強面、心は少年の西川さんの\n' +
        '「BB  LABO.」をよろしくお願いします。\n' +
        '\n' +
        '西川さん、また顔出しまーす！',
      pic: require('../assets/images/interview/S__27918372.jpg'),
    },
    {
      id: 7,
      name: '香月 良太',
      title: '元読売ジャイアンツ',
      subTitle: '',
      message:
        '西川とは、同級生でもあり同じピッチャーで切磋琢磨した仲です。\n' +
        '遠征先では、食事をしながら反省会をしていたのが懐かしいです。\n' +
        '体と心の軸を大切に、こだわりを持ってとことんやれよ！！',
      pic: require('../assets/images/interview/S__27918374.jpg'),
    },
    {
      id: 8,
      name: '清水 章夫',
      title: '元オリックス･バファローズ',
      subTitle: '',
      message:
        'プロのピッチャーのトレーニングで大切な事は、強くてしなやかで、何よりもケガをしない体づくりです。\n' +
        'プロ野球で学んだトレーニングを存分に活かして、未来のプロ野球選手の力になれるように尽力してください。\n' +
        'また姫路に行く時は遊びに行きます。',
      pic: require('../assets/images/interview/S__27918376.jpg'),
    },
    {
      id: 9,
      name: '岩崎 哲也',
      title: '元西武ライオンズ',
      subTitle: '',
      message:
        '西川と共にプレーしたのは独立リーグでの1年でした。もう1度NPBに戻るため、環境に妥協せず意識を高くもって過ごした時間を鮮明に覚えてるよ。\n' +
        'あの経験は今でも心支えになってるよ。今までは自分のため、チームのため、ファンのために頑張ってきたけどこれからはお客様のために頑張れよ。',
      pic: require('../assets/images/interview/S__27918378.jpg'),
    },
    {
      id: 10,
      name: '播戸 竜二',
      title: '元プロサッカー選手',
      subTitle: '',
      message:
        '西川代表とは、かれこれ36年の付き合いになります。\n' +
        '弟のように可愛がってきた幼なじみです。\n' +
        '私は『 サッカー 』西川代表は『 野球 』というスポーツで、まさか2人ともプロの世界に進むなんて、今思えば凄いことです。\n' +
        '体づくりで多くの人を喜ばせ、また、野球指導では、プロで培った信念を持って、姫路のため、ひいては日本の野球界のために頑張って欲しいです。応援しています！',
      pic: require('../assets/images/interview/S__27918380.jpg'),
    },
  ]
}
</script>

<style lang="scss" scoped>
.mini-profile {
  width: 50%;
}
.a{
  text-decoration: none;
}
</style>
