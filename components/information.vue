<template>
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
    <h4><strong>新型コロナウイルス蔓延予防のための県有施設の休館について</strong></h4>
      <p class="support">新型コロナウイルスに関する緊急事態宣言の対象地域が全国に拡大され，本県を含む１３都道府県が感染防止対策の取組を重点的に進める「特定警戒都道府県」に指定されたことを受け，次の県有施設について４月１８日から５月６日まで休館とします</p>
    <h5><strong>休館する施設</strong></h5> 
      <p class="support">県立図書館，県近代美術館（本館・つくば美術館・天心記念五浦美術館）県陶芸美術館，県立歴史館，国民宿舎「鵜の岬」，レイクビュー水戸</p>
  </div>
</template>


<script>
    export default {
  name: "Information"
}
</script>


<style>

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
  padding: 22px; 
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
.prevent {
  width: 30%;
  height: 100%; 
  display: inline-block; 
}
</style>