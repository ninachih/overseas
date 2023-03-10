<template>
    <div id="count">
       <div class="notice">
            <img src="../assets/attention.svg" alt="">
            <p class="red">提醒您，(多人一起投保)需要在(2022/04/17_12:00)前簽回要保書</p>
        </div>
        <div class="countPrize">
            <div class="countCon">
                <p>總計保費</p>
                <p class="prize">$388 / 6人</p>
            </div>     
        </div>
    </div>
</template>
<script>
export default {
  name: "count",
}
</script>

<style lang="scss">
#count{
   display:flex;
   margin:30px 0;
   .red{
    color:$pink
   }
   .notice{
    width:45%;
    display: flex;
    vertical-align: top;
    p{margin-left:35px}
    img{width:30px;position:absolute;}
    p,img{display:inline-block}
   }
   .countPrize{
    width:55%;
    .countCon{
        float:right;
        border: 4px solid $mainBlue;
        color:$mainBlue;
        border-radius: 10px;
        padding:5px;
        width: 300px;
        box-sizing: border-box;
        font-weight:bold;
        .prize{
            font-size:32px;
            color:$pink;
            text-align:right
        }
    }
   }
}
</style>