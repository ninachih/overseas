<template>
    <div id="count2">
      <goTop/>
      <step/>
      <div class="content">
        <div class="container">
          <h2 class="title2">保費試算</h2>
          <attention/>
          <h3 class="countTitle">國外旅行綜合險保費快算</h3>
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
        <router-link :to="'/detail'" class="btn center">立即投保<img src="../assets/go.svg" alt=""></router-link>
        <div class="anotherBtn">
          <router-link :to="'/count1'" class="btn">返回</router-link>
          <router-link :to="'/adjustment'" class="btn">微調保障</router-link>
      </div>
      </div>    
    </div>
</template>
<script>
import goTop from "@/components/gotop.vue";
import step from "@/components/step.vue";
import attention from "@/components/attention.vue";
import count from "@/components/count.vue";

export default {
  name: "count2",
  data() {
    return {
      prizeRange1:[
       {prize:'100萬'},
       {prize:'200萬'},
       {prize:'300萬'},
       {prize:'400萬'},
       {prize:'500萬'},
       {prize:'600萬'},
       {prize:'700萬'},
       {prize:'800萬'},
       {prize:'900萬'},
       {prize:'1000萬'},
       {prize:'1100萬'},
       {prize:'1200萬'}, 
       {prize:'1300萬'}, 
       {prize:'1400萬'}, 
       {prize:'1500萬'}, 
      ],
      prizeRange2:[
       {prize:'10萬'},
       {prize:'20萬'},
       {prize:'30萬'},
       {prize:'40萬'},
       {prize:'50萬'},
       {prize:'60萬'},
       {prize:'70萬'},
       {prize:'80萬'},
       {prize:'90萬'},
       {prize:'100萬'},
       {prize:'110萬'},
       {prize:'120萬'}, 
       {prize:'130萬'}, 
       {prize:'140萬'}, 
       {prize:'150萬'}, 
      ],
      isActive:false,
      plan:[
        {
          id:0,
          plan_title: "其他費用補償保險",
          isCheck:false,
          planName:"plan1",
          plan_content:[
            {
              listItem:"食物中毒費用保險(定額)",
              listPrize:"3,000"
            },
            {
              listItem:"旅行期間居家竊盜保險(限額)",
              listPrize:"50,000"
            },
            {
              listItem:"現金竊盜損失險(限額)",
              listPrize:"3,000"
            },
            {
              listItem:"信用卡盜用損失保險(限額)",
              listPrize:"20,000"
            },
            {
              listItem:"班機改降補償保險(定額)",
              listPrize:"1,000"
            },
            {
              listItem:"劫持事故補償保險(定額)",
              listPrize:"100,000"
            }
          ]
        },
        {
          id:1,
          plan_title: "海外突發疾病險",
          isCheck:false,
          planName:"plan2",
          plan_content:[
              {
                listItem:"住院醫療費用保險金",
                listPrize:"100,000"
              },
              {
                listItem:"門診醫療費用保險金",
                listPrize:"1,000"
              },
              {
                listItem:"急診醫療費用保險金",
                listPrize:"1,000"
              }
          ]
        },
        {
          id:2,
          plan_title: "緊急醫療救援費用保險 ",
          isCheck:false,
          planName:"plan3",
          plan_content:[
            {
              listItem:"緊急醫療救援費用保險 ",
              listPrize:"一般國家60萬<br>申根國家60萬或150萬"
            }
          ]
        }
      ],
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
   planSelect(event,planIndex,item){
    this.isActive = !this.isActive;
    item.isCheck = !item.isCheck;
    console.log(planIndex,item.isCheck);
    var vm = event.target;
    var planCon = $(vm).next('.planCon');
    $(vm).parent('.plan').toggleClass('active');
    planCon.slideToggle();
  
   }
  
  }
};
</script>
<style lang="scss">
#count2{
  color:$deepGray;
  .mainPlan{ 
      border:2px solid $mainBlue;
      background:#fff;
      width:95%;
      border-radius:10px;
      overflow: hidden;
      margin:30px auto; 
      .planTitle{background:$mainBlue;
        &::after{
          content:"";
          display:block;
          position:absolute;
          right:20px;
          top:10px;
          width:30px;
          height:30px;
          background-image:url(../assets/isChoose.svg);
          background-repeat: no-repeat;
        }
        input[type="checkbox"]{
          display:none;
        }
      }
      ul{
      box-sizing: border-box;
      padding:0 20px;
        li{
          display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-pack: justify;
            -ms-flex-pack: justify;
            justify-content: space-between;
            line-height:40px;
            font-weight:bold;
            padding:3px 0;
            .inputStyle{
              width:40%;
            }
        }
    }
  }
  .plan{
    margin:30px auto;
    cursor: pointer;
    width:95%;
    border-radius:10px;
    overflow: hidden;
    background:$gray;
    .goDate,.goCountry{margin:10px 0}
    &.active{
      border:2px solid $mainBlue;
      background:#fff;
      .planTitle{
        background:$mainBlue;
        box-sizing: border-box;
        padding:10px 20px;
        margin-bottom:10px;
        &::after{
          background-image:url(../assets/isChoose.svg);
          background-repeat: no-repeat;
        }
      }
    }
    ul{
      box-sizing: border-box;
      padding:0 20px;
        li{
          display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-pack: justify;
            -ms-flex-pack: justify;
            justify-content: space-between;
            line-height:40px;
            font-weight:bold;
            padding:3px 0;
            .inputStyle{
              width:40%;
            }
        }
    }
  }
  .planTitle{
      background:$gray;
      box-sizing: border-box;
      padding:10px 20px;
      position:relative;
      p{padding-left:10px;color:#fff;border-left:3px solid #fff;display:inline-block;margin-right:5px;}
      &::after{
        content:"";
        display:block;
        position:absolute;
        right:20px;
        top:10px;
        width:30px;
        height:30px;
        background-image:url(../assets/add.svg);
        background-repeat: no-repeat;
      }
  }
  .planCon{
      display:none;
  }
  .choose{
    opacity:0
  }
  
}
</style>
