<template>
  <div id="app">
   <input type="text" v-model="text">
   <button @click="getaddress">住所入力</button>
   <p>Address:{{address}}</p>
  </div>
</template>

<script>
import axios from "axios";
export default{
  data(){
    return{
      text:"",
      address:""
    };
  },
  async getaddress(){
    const res =await axios.get(`https://apis.postcode-jp.com/api/v4/postcodes/${this.text}?apiKey=bPRFvyBgjHxi0hvGJuY7O676Y9cNPnEVs8ejjmj`);
    console.log(res);

  }
};
</script>

