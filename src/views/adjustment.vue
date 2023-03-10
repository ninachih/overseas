<template>
    <div id="adjustment">
      <goTop/>
      <step/>
      <div class="content">
        <div class="container">
          <h2 class="title2">保障調整</h2>
          <attention/>
          <h3 class="countTitle">旅客投保旅平綜合保險保障明細</h3>
          <p class="goCountry">旅遊國家 : <span>日本</span> / <span>韓國</span></p>
          <p class="goDate">旅遊期間 : <span>2023-04-11 10:00</span> ~ <span>2023-04-18  10:00</span></p>
          
          <div class="form">
           
            
          </div>
          <div class="greenLine"></div>
          <count/>
        </div>  
      </div>
      <div class="btnArea">
        <router-link :to="'/count2'" class="btn center">試算我的保費<img src="../assets/go.svg" alt=""></router-link>
      </div>    
    </div>
</template>
<script>
import goTop from "@/components/gotop.vue";
import step from "@/components/step.vue";
import attention from "@/components/attention.vue";
import count from "@/components/count.vue";
export default {
  name: "adjustment",
  data() {
    return {
      
    }
  },
  components: {
    goTop,
    step,
    attention,
    count
  },
  mounted() {
    $("#step li:nth-of-type(1)").find(".number").addClass('active'); //設定哪個step亮黃圈
  },
  methods: {
  
  
  }
};
</script>
<style lang="scss">
#adjustment{
 
  
  
}
</style>
