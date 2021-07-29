<template>
<!--  <h1>Hello, {{title}}!</h1>-->
<!--  String data binding-->
<!--  <div>
    <div>{{htmlString}}</div>
    <div v-html="htmlString"></div>
  </div>-->
<!--  raw html data binding-->
  <div>
    <input type="text" v-model="valueModel">
  </div>
  <div>
    <input type="number" v-model.number="numberModel">
  </div>
  <div>
    <textarea v-model="message"></textarea>
  </div>
  <div>
    <select v-model="city">
      <option value="02">서울</option>
      <option value="21">부산</option>
      <option value="064">제주</option>
    </select>
  </div>
  <div>
    <label>
      <input type="checkbox" v-model="checked" true-value="yes" false-value="no"> {{checked}}
    </label>
  </div>
  <div>
    <label><input type="checkbox" value="서울" v-model="multiChecked">서울</label>
    <label><input type="checkbox" value="부산" v-model="multiChecked">부산</label>
    <label><input type="checkbox" value="제주" v-model="multiChecked">제주</label>
    <br>
    <span>체크한 지역 : {{multiChecked}}</span>
  </div>
  <div>
    <label><input type="radio" v-bind:value="radioValue1" v-model="picked"> 서울</label>
    <label><input type="radio" v-bind:value="radioValue2" v-model="picked"> 부산</label>
    <label><input type="radio" v-bind:value="radioValue3" v-model="picked"> 제주</label>
    <br>
    <span>선택한 지역 : {{picked}}</span>
  </div>
<!--  input form binding-->
</template>

<script>
  export default {
    data() {
      return {
        //title : 'world' // String data binding
        //htmlString : '<p style="color: red;">This is a red string.</p>' // raw html data binding
        valueModel : 'South Korea',  // input form binding
        numberModel : 3,  // input form binding
        message : "여러 줄을 입력할 수 있는 textarea 입니다.",  // input form binding
        city : "064",  // input form binding
        checked : true,  // input form binding
        multiChecked : [],  // input form binding
        picked : '',  // input form binding
        radioValue1 : '서울',  // input form binding
        radioValue2 : '부산',  // input form binding
        radioValue3 : '제주',  // input form binding
      };
    }
  }
</script>
