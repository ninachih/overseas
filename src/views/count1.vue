<template>
  <div id="count1">
    <goTop/>
    <step/>
    <div class="content">
      <div class="container">
        <h2 class="title2">保費試算</h2>
        <attention/>
        <h3 class="countTitle">國外旅行綜合險保費快算</h3>
        <ul class="topBtn">
          <li v-for="item in collection"
          :class="{'active': current === item.id}"
          @click="topBtnEffect(item.id)">
          {{item.name}}
          </li>
        </ul>
        <div class="form">
          <div class="inline">
            <div class="inputControl">
              <div class="inputTitle">旅遊國家 <img src="../assets/attention.svg" alt="" class="attention"></div>
              <input readonly class="inputStyle arrow" value="日本" @click="toggle">
              <countrySelect v-if="showPopup"/>
              <div id="countrySearch"></div> 
            </div>
            <div class="inputControl">
              <div class="inputTitle">投保人數 <img src="../assets/attention.svg" alt="" class="attention"></div>
              <input readonly class="inputStyle arrow">
            </div>
          </div>
          <div class="inline">
            <div class="inputControl">
              <div class="inputTitle">旅遊期間(保險期間) <img src="../assets/attention.svg" alt="" class="attention"></div>
              <input id="startEndDate" class="inputStyle calendar" value="" placeholder="請選擇從家中出發至返家日期">
            </div>
            <div class="inputControl">
              <div class="inputTitle"></div>
              <select class="inputStyle arrow">
                <option value="" disable selected>請選擇時間</option>
                <option :value="item.time" v-for="item in timeRange">{{item.time}}</option>
              </select>
            </div>
          </div>
          <div class="inline">
            <div class="inputControl">
              <div class="inputTitle">保險期間</div>
              <input readonly class="inputStyle red" value="2022/04/11_10:00-2022/04/18_10:00 共7天">
            </div>
            <div class="inputControl">
              <div class="inputTitle">活動代碼</div>
              <input type="text" placeholder="非必填" class="inputStyle">
            </div>
          </div>
        </div>
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
import countrySelect from "@/components/countrySelect.vue";
import moment from 'moment';

export default {
  name: "count1",
  components:{
    goTop,
    step,
    attention,
    countrySelect        
  },
  data(){
    return{
      current: 2,
      collection: [
        {id: 1, name: '多人一起保'},
        {id: 2, name: '幫自己保'},
        {id: 3, name: '幫他人保'},
      ],
      range: ["", ""],
      options: {
        showDropdowns: true,
        minYear: 2023,
        locale: {
          format: 'YYYY-MM-DD mm:ss'
        }
      },
      timeRange:[
       {time:'00:00'},{time:'01:00'},{time:'02:00'},{time:'03:00'},{time:'04:00'},{time:'05:00'},{time:'06:00'},
       {time:'07:00'},{time:'08:00'},{time:'09:00'},{time:'10:00'},{time:'11:00'},{time:'12:00'},{time:'13:00'},
       {time:'14:00'},{time:'15:00'},{time:'16:00'},{time:'17:00'},{time:'18:00'},{time:'19:00'},{time:'20:00'},
       {time:'21:00'},{time:'22:00'},{time:'23:00'},{time:'24:00'}
      ],
      showPopup: false
    }
  },
  mounted(){
    $("#step li:nth-of-type(1)").find(".number").addClass('active'); //設定哪個step亮黃圈 
    this.daterangepicker();
    $('#startEndDate').val("");
  },
  methods:{
    topBtnEffect(id){
      this.current = id;
    },
    daterangepicker(){
      $('#startEndDate').daterangepicker({
          maxYear:moment().format('YYYY'),
          locale: {
            format: 'YYYY-MM-DD'
          }
      });
      
      $('#startEndDate').on('apply.daterangepicker', function(ev, picker) {
          $(this).val(picker.startDate.format('YYYY-MM-DD') + ' ~ ' + picker.endDate.format('YYYY-MM-DD'));
      });

      $('#startEndDate').on('cancel.daterangepicker', function(ev, picker) {
          $(this).val('');
      });
    },
    toggle(){
       $("#countrySelect").slideToggle();
       this.showPopup = !this.showPopup
    },
    
    close(el){
        this.showPopup = false
    }
  }
 
};
</script>
<style lang="scss">
#count1{
 .topBtn{
  width:420px;
  margin:0 auto;
  border: 1px solid $gray;
  border-radius: 30px;
  overflow:hidden;
  display: flex;
  li{
    color:$gray;
    font-size:18px;
    border-radius: 30px;
    width:33.3333%;
    text-align:center;
    padding:15px 0;
    cursor: pointer;
    font-weight:bold;
    &.active{background:$mainBlue;color:#fff;transition: all 300ms ease-in-out;}
  }
 }

}

</style>