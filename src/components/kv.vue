<template>
<div class="kv">
    <img src="../assets/kvTxt.svg" alt="" class="title">
    <div class="container">
      <div class="btnArea center">
        <router-link :to="{ path: '/', hash: '#travelTheme' }" class="btn">跟著旅程買 <img src="../assets/go.svg" alt=""></router-link>
        <router-link :to="'/count1'" class="btn">立即投保<img src="../assets/go.svg" alt=""></router-link>
      </div>
    </div>
    
</div>
</template>
<script>
export default {
  name: "kv"
}
</script>
<style lang="scss">
.kv {
   background:url("../assets/KV.svg");
   background-color:#cceff2;
   background-size: contain;
   background-repeat: no-repeat;
   background-position: center top;
   margin-top:95px;
   padding:0 0 10%;
   text-align:center;
   @media screen and (max-width: $small) {
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center top;
   }
  .bg{position:relative;top:0;z-index: 10;}
  .title{
    display:inline-block;
    margin:0 auto;
    padding:3% 0;

  @media screen and (max-width: $small) {
     width:250px;
     padding:20% 0 80%;
   }
  }
}
</style>
