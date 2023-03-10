<template>
     <div id="countrySelect">
        <b-tabs card>
          <b-tab :title="tab.tab_title" v-for="(tab, index) in tabs" :key="index">
          <div v-html="tab.tab_content"></div>
        </b-tab>
          
        </b-tabs>
    </div>
</template>

<script>

export default {
  name: "countrySelect",
  mounted(){  
    
  },
  data(){
    return{
        tabs:[
            {
            tab_title: "熱門旅遊地",
            tab_content:"<ul class='countryList'><li>日本</li><li>中國大陸</li><li>香港</li><li>韓國</li><li>泰國</li></ul>"
            },
            {
            tab_title: "亞洲",
            tab_content:
                "<ul class='countryList'><li>中國大陸</li><li>日本</li><li>香港</li><li>韓國</li><li>沙地阿拉伯</li><li>柬埔寨</li><li>印度</li><li>印尼</li><li>寮國</li><li>黎巴嫩</li><li>澳門</li><li>蒙古</li<li>緬甸</li><li>巴基斯坦</li><li>菲律賓</li><li>卡達</li><li>俄羅斯</li><li>新加坡</li><li>亞克羅提利與德凱利亞</li><li>葉門</li><li>越南</li></ul>"
            },
            {
            tab_title: "歐洲",
            tab_content:
                "<ul class='countryList'><li>奧地利</li><li>比利時</li><li>保加利亞</li><li>克羅埃西亞</li><li>賽普勒斯</li><li>捷克</li><li>丹麥</li><li>愛沙尼亞</li><li>芬蘭</li><li>法國</li><li>德國</li><li>希臘</li><li>匈牙利</li><li>愛爾蘭</li><li>義大利</li><li>拉脫維亞</li></ul>"
            },
            {
            tab_title: "美洲",
            tab_content:
            "<ul class='countryList'><li>加拿大</li><li>美國</li><li>巴西聯邦共和國</li><li>巴拉圭</li><li>委內瑞拉</li><li>阿根廷</li><li>哥倫比亞</li><li>烏拉圭</li><li>秘魯</li><li>智利</li><li>巴拿馬</li><li>尼加拉瓜</li><li>瓜地馬拉</li><li>多明尼加</li><li>宏都拉斯</li><li>哥斯大黎加</li><li>墨西哥</li><li>薩爾瓦多</li></ul>"
            },
            {
            tab_title: "其他",
            tab_content:
            "<ul class='countryList'><li>史瓦帝尼</li><li>布吉納法索</li><li>奈及利亞</li><li>肯亞</li><li>紐西蘭</li><li>斐濟</li><li>澳大利亞</li><li>不丹</li><li>巴基斯坦伊斯蘭共和國</li><li>馬爾地夫共和國</li><li>帛琉</li><li>吐瓦魯</li></ul>"
            } 
        ]
    }
  },
  methods:{
   
  }
 
  
};
</script>

<style lang="scss">
#countrySelect{
   position:absolute;
   background: #FFFFFF;
   border: 1px solid $gray;
   border-top:0;
   border-radius: 10px;
   width:100%;
   z-index: 100;
   box-sizing: border-box;
   padding:10px 10px 20px;
   font-size:14px;
   .card-header{
    &::after{
      content:"";
      display:block;
      border-bottom:1px solid #e8e8e8;
      margin:10px 0;
      width:100%;
      }
   }
   .nav-tabs{
    li{
      display: inline-block;
      a{ 
        border: 1px solid $btnGray;
        border-radius: 20px;
        text-align: center;
        display:block;
        width: auto;
        box-sizing: border-box;
        padding:2px 20px;
        margin:3px;
        color:$deepGray;
        &.active{
          background:$mainBlue;
          color:#fff;
          border:1px solid $mainBlue;
        }
      }
     
    }
   }
   .tab-content{
      max-height:200px;
      overflow-y:auto;
      &::-webkit-scrollbar {
        width: 5px;
        height: 8px;
        background: $btnGray;
        border-radius:10px;
      }
      &::-webkit-scrollbar-thumb {
          border-radius:10px;
          background-color: $mainBlue; 
          margin-right:10px;
      }
   }
   .countryList{
    border: 1px solid $btnGray;
    border-radius: 10px;
    overflow:hidden;
    margin:0 5px;
      li{
        float:left;
        width:50%;
        border:1px solid #e8e8e8;
        box-sizing: border-box;
        padding:5px;
        text-align: center;
        cursor: pointer;
        &:hover{
          background:$mainBlue;
          color:#fff;
        }
      }

   }
}
</style>