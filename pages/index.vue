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
  <Information></Information> 
  </div>
</template>

<script>
    import Header from "~/components/Header"
    import Information from "~/components/Information"
export default {
  name: "Index",
  components: { Header, Information, },
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

.question{
  text-align: center; 
  font-family: "Times New Roman", Times, serif;
  font-size: 18px; 
  padding-top: 43px; 
  padding-bottom: 43px; 
  background-color: #B2EBF2; 
  color: #367588; 
}

.question2{
  text-align: center; 
  font-family: "Times New Roman", Times, serif;
  font-size: 18px; 
  padding-top: 43px; 
  padding-bottom: 43px; 
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


</style> 