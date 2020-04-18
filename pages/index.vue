<template>
  <div class="full">
    <Header></Header>
  <div class="site">
    <div class="question">
      <input type="checkbox" v-model="select1" @change="calc" /> 熱は37.5度以上ある
      {{ select1 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select2" @change="calc" /> 匂いの感覚がない
      {{ select2 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select3" @change="calc" /> 味の感覚がない
      {{ select3 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select4" @change="calc" /> 喉の痛みや咳などの症状がある
      {{ select4 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select5" @change="calc" /> 呼吸困難を感じている
      {{ select5 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select6" @change="calc" /> 鼻水などの症状がある
      {{ select6 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select7" @change="calc" /> 胸のあたりに痛みがある
      {{ select7 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select8" @change="calc" /> 腹痛がある
      {{ select8 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select9" @change="calc" /> 胃のむかつきや食欲不振が続いている
      {{ select9 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select10" @change="calc" /> 頭痛などの症状がある
      {{ select10 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select11" @change="calc" /> 筋肉痛の症状がある（運動や行動以外の事で）
      {{ select11 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select12" @change="calc" /> 非常に疲れていたり、エネルギー不足を感じている
      {{ select12 }}
    </div>

    <div class="result">
      <button @click="diagnosis" class="button">診断結果</button> 
    </div>
  </div>
  <div class="prevent">
    <h2 class="emergency"><strong>茨城県における緊急事態措置等</strong></h2>
    <ol class="infor">
      <li>実施期間：2020年４月18日（土）から５月６日（水）まで</li>
      <li>対象地域：茨城県全域　</li>
      <li>実施概要：外出自粛や通勤・通学自粛等の要請、複数の者が参加し，密集状態等が発生する恐れのあるイベント等の開催自粛の要請、別紙の施設に対する休業の要請</li>
      <li>協力金：１事業者 最大30万円（１事業者当たり10万円。事業所を賃借している場合は10万円を加算。複数賃借している場合はさらに10万円を加算）</li>
    </ol>
    <h2 class="emergency"><strong>茨城県にお住いの皆様へ</strong></h2>
    <p class="notice">緊急事態措置では，国の方針に基づき，必要最小限のものとし，以下の３点を要請します。</p>
    <ul class="information">
      <li>茨城県にお住いの方に対する外出自粛要請</li>
      <li>「３つの密」が重なりやすい施設に対する休業要請</li>
      <li>「３つの密」が重なりやすい施設でのイベントの開催自粛</li>
    </ul>
    <h6><strong>＜ポイント＞</strong> </h6>
      <p class="notice">社会生活を維持する上で必要な施設（医療施設，生活物資販売施設，食事提供施設，交通機関等）については，感染防止対策を講じて事業を継続します。</p>
      <p class="important" style="border:3px; border-style:solid; border-color:#FF0000; padding: 5px; margin: 7px; "> 食料・医薬品や生活必需品は，これまでどおり店頭で購入できますので，買い占め等で混乱が生じないよう，冷静な購買活動にご協力ください。</p>
    <h4><strong>休業要請する施設の具体例</strong></h4>
    <ul class="information">
      <li>遊技施設：パチンコ店</li>
      <li>遊興施設等：キャバレー，ナイトクラブ，ダンスホール，スナック（接待を伴うものに限る。），バー（接待を伴うものに限る。），ダーツバー，パブ，性風俗店，デリヘル，アダルトショップ，個室ビデオ店，カラオケボックス，ライブハウス</li>
      <li>劇場等：劇場，観覧場，プラネタリウム，映画館，演芸場</li>
      <li>運動・遊技施設 ：スポーツクラブ，ホットヨガ，ヨガスタジオ，マージャン店，ゲームセンター</li>
    </ul>
    <h5><strong>休業要請及び協力金に関するお問い合わせはこちら</strong></h5>
      <p class="support">緊急事態宣言を受けて，事業者の皆様からの休業要請や協力金に関する相談に対応する専用相談窓口を４月１８日（土）から開設します。<br></br> 開設時間 ９時～１７時（土日祝日を含む毎日）電話番号 ０２９ー３０１ー５３７５</p>
  </div>
  </div>
</template>

<script>
    import Header from "~/components/Header"
export default {
  name: "Index",
  components: { Header },
    data(){
       return{
         select1: false,
         select2: false,
         select3: false,
         select4: false,
         select5: false,
         select6: false, 
         select7: false, 
         select8: false, 
         select9: false,
         select10: false, 
         select11: false, 
         select12: false, 
         point: 0, 
       }
    }, 
    methods: {
      calc() {
          console.log(this.select1)
          this.point = 0
          if (this.select1 === true){
             this.point += 10 
          }
          if(this.select2 === true) {
              this.point += 10  
          }
          if(this.select3 === true) {
              this.point += 10
          }
          if(this.select4 === true) {
              this.point += 10
          }
          if(this.select5 === true) {
              this.point += 10
          }
          if(this.select6 === true) {
              this.point += 5
          }
          if(this.select7 === true) {
              this.point += 10
          }
          if(this.select8 === true) {
              this.point += 5
          }
          if(this.select9 === true) {
              this.point += 5
          }
          if(this.select10 === true) {
              this.point += 10
          }
          if(this.select11 === true) {
              this.point += 5
          }
          if(this.select12 === true) {
              this.point += 10
          }
          
          console.log(this.point)
      },
      diagnosis(){
        alert("診断します！")
        alert("あなたは" + this.point + "%コロナです")
      }
        
    }
  }

</script>

<style scooped>

.full{
  height: 100%;
  width: 100%;
  display: inline-block; 
}

.site{
  width: 70%; 
  height: 100%; 
  display: inline-block; 
  float: left; 
}

.prevent {
  width: 30%;
  height: 100%; 
  display: inline-block; 
}

.question{
  text-align: center; 
  font-family: "Times New Roman", Times, serif;
  font-size: 18px; 
  padding-top: 25px; 
  padding-bottom: 25px; 
  background-color: #B2EBF2; 
  color: #367588; 
}

.question2{
  text-align: center; 
  font-family: "Times New Roman", Times, serif;
  font-size: 18px; 
  padding-top: 25px; 
  padding-bottom: 25px; 
  background-color: #367588; 
  color: #B2EBF2; 
}
.result{
  text-align: center; 
  padding-top: 25px; 
  padding-bottom: 30px; 
  background-color: #B2EBF2; 
  color: #367588; 
}

.button {
  color: #367588; 
}

.wash{
  margin-left: auto;
  margin-right: auto;
  display: block;
  width: 100%;
}

.wash2{
  margin-left: auto;
  margin-right: auto;
  display: block;
  width: 100%;
}

.descript{
  text-align: center; 
  color: #367588;
  padding: 7px 5px; 
  font-size: 15px; 
}

.emergency{
  font-size: 25px; 
  text-align: center;
  font-family: "Times New Roman", Times, serif;
  padding: 6px; 
}
.infor{
  text-align: left; 
  padding-bottom: 5px; 
  width: 95%;
  padding-left: 40px; 
}

.notice{
   width: 95%;
   text-align: center; 
}

.important{
  border-width: 3px; 
  border-color: red; 
  padding: 5px 9px; 
}

.information{
  padding: 9px; 
}

h4 {
  text-align: center; 
  padding: 5px; 
}

h5 {
  text-align: center; 
  padding: 5px; 
}
.support{
  padding: 5px; 
}

</style> 