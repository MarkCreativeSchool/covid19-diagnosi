<template>
　<div class="head">
    <div class="title">
        <h1>COVID19 DIAGNOSIS/コロナ診断</h1> 
    </div>
    <div class="info">
        この診断はコロナに観戦しているか簡単に診断するサイトです。以下の質問の内容・症状が３日以上続いている方はチェックボックスに記入してください。しかし、これはプロジェクトのために作成したものなので、内容や情報が間違っています。もし、高い割合で感染してると診断されていても信じないでください。
    </div>  
  </div> 
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scooped>

.head{
    height: 180px;
    width: 100%; 
    background-color: #013c47; 
    color: #B2EBF2; 
    position: relative; 
    padding-left: 10px; 
    padding-right: 10px; 
    padding-top: 15px; 
}
.title{
    font-size: 30px; 
    text-align: center; 
    color: #B2EBF2; 
    font-family: "Times New Roman", Times, serif;
}

.info{
    font-size: 18px; 
    text-align: center; 
    font-family: "Times New Roman", Times, serif;
}

</style> 