<template>
  <div class="site">
    <Header></Header>
    <div class="question">
      <input type="checkbox" v-model="select1" @change="calc" /> 熱は37.5度以上在りますか？
      {{ select1 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select2" @change="calc" /> 味覚は在りますか？
      {{ select2 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select3" @change="calc" /> 嗅覚は在りますか？
      {{ select3 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select4" @change="calc" /> 喉の痛みや咳などの症状は在りますか？
      {{ select4 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select5" @change="calc" /> 呼吸に問題は在りますか？
      {{ select5 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select6" @change="calc" /> 鼻水などの症状は在りますか？
      {{ select6 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select7" @change="calc" /> 胸のあたりに痛みは在りますか？
      {{ select7 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select8" @change="calc" /> 腹痛は在りますか？
      {{ select8 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select9" @change="calc" /> 胃のむかつきや食欲不振はありましたか？
      {{ select9 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select10" @change="calc" /> 頭痛などの症状が在りますか？
      {{ select10 }}
    </div>
    <div class="question">
      <input type="checkbox" v-model="select11" @change="calc" /> 筋肉痛の症状はありますか？（運動や行動以外の事で）
      {{ select11 }}
    </div>
    <div class="question2">
      <input type="checkbox" v-model="select12" @change="calc" /> 非常に疲れていたり、エネルギー不足を感じていませんか
      {{ select12 }}
    </div>

    <div class="result">
      <button @click="diagnosis" class="button">診断結果</button> 
    </div>
  </div>
</template>

<script>
    import Header from "~/components/Header"
export default {
    data(){
       return{
         select1: true,
         select2: true,
         select3: true,
         select4: true,
         select5: true,
         select6: true,
         select7: true, 
         select8: true,
         select9: true,
         select10: true,
         select11: true,
         select12: true,
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

.site{
  width: 100%; 
  height: 100%; 
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

</style> 