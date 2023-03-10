<template>
    <div id="detail">
      <goTop/>
      <step/>
      <div class="content">
        <div class="container">
          <h2 class="title2">填寫資料</h2>
          <h3 class="countTitle">要保人資料</h3>
          <p class="goCountry">旅遊國家 : <span>日本</span> / <span>韓國</span></p>
          <p class="goDate">旅遊期間 : <span>2023-04-11 10:00</span> ~ <span>2023-04-18  10:00</span></p>
          <h2 class="title3">選擇旅平險保障</h2>
          <div class="greenLine"></div>
          <div class="form">
            <div class="inline">
              <div class="inputControl">
                <div class="inputTitle">意外死亡及失能 <img src="../assets/question.svg" alt="" class="question"></div>
                <select class="inputStyle arrow">
                <option value="" disable selected>100萬</option>
                <option :value="item.time" v-for="item in prizeRange1">{{item.prize}}</option>
              </select>
              </div>
              <div class="inputControl">
                <div class="inputTitle">傷害醫療 <img src="../assets/question.svg" alt="" class="question"></div>
                <select class="inputStyle arrow">
                  <option value="" disable selected>10萬</option>
                  <option :value="item.time" v-for="item in prizeRange2">{{item.prize}}</option>
                </select>
              </div>
            </div>
            <div class="inline">
              <div class="inputControl">
                <div class="inputTitle">個人賠償責任(每一事故自負額2,500元) <img src="../assets/question.svg" alt="" class="question"></div>
                <input readonly class="inputStyle" value="體傷20萬 / 財損10萬 / 最高60萬">
              </div>
              <div class="inputControl"></div>
            </div>
            <h2 class="title3">選擇旅遊不便險方案</h2>
            <div class="greenLine"></div>
            <div class="mainPlan active">
              <div class="planTitle"><p>國外旅遊不便險</p><img src="../assets/question.svg" alt="" class="question"> <input type="checkbox" class="choose" checked></div>
              <ul>
                <li><p>班機延誤保險(限制4小時)</p>
                  <select name="" id="" class="inputStyle arrow">
                    <option value="定額6,000">定額6,000</option>
                    <option value="定額12,000">定額12,000</option>
                    <option value="限額30,000">限額30,000</option>
                    <option value="限額50,000">限額50,000</option>
                  </select>
                </li>
                <li><p>行李延誤費用保險</p><p>定額6,000</p></li>
                <li><p>行李損失保險 (定額) </p><p>6,000</p></li>
                <li><p>旅行文件損失保險(定額) </p><p>6,000</p></li>
                <li><p>旅程取消費用保險(限額)</p><p>30,000</p></li>
                <li><p>旅程更改費用保險(限額)</p><p>30,000</p></li>
              </ul>
            </div>
            <h2 class="title3">加購其他險種</h2>
            <div class="greenLine"></div>
            <div class="plan" @click="planSelect($event,plan_index,item)" v-for="(item,plan_index) in plan" :key="plan_index">
              <div class="planTitle">
                <p>{{ item.plan_title }}</p><img src="../assets/question.svg" alt="" class="question"> 
                <input type="checkbox" class="choose" :name="item.planName" :checked="item.isCheck">
              </div>
              <ul class="planCon">                                                                                      
                <li v-for="(planCon,planCon_index) in item.plan_content" :key="planCon_index"><p>{{planCon.listItem}}</p><p v-html="planCon.listPrize"></p></li>
              </ul>
            </div>
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

export default {
  name: "detail",
  data() {
    return {
      
    }
  },
  components: {
    goTop,
    step,

  },
  mounted() {
    $("#step li:nth-of-type(2)").find(".number").addClass('active'); //設定哪個step亮黃圈
  },
  methods: {
  
  
  }
};
</script>
<style lang="scss">
#detail{
 
  
  
}
</style>
