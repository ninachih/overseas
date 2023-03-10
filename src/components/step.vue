<template>
    <div id="step">
            <ul>
                <li>
                    <div class="number">1</div>
                    <p>保費試算</p>
                </li>
                <li>
                    <div class="number">2</div>
                    <p>填寫資料</p>
                </li>
                <li>
                    <div class="number">3</div>
                    <p>告知事項</p>
                </li>
                <li>
                    <div class="number">4</div>
                    <p>確認資料</p>
                </li>
                <li>
                    <div class="number">5</div>
                    <p>投保繳費</p>
                </li>
                <li>
                    <div class="number">6</div>
                    <p>完成投保</p>
                </li>
            </ul>
    </div>
</template>
<script>
export default {
  name: "step",
}
</script>

<style lang="scss">
#step{
    padding-top:100px;
    width:600px;
    margin:50px auto;
    position:relative;
    &::after{
        content: "";
        display: block;
        border-top: 2px solid #CACCCF;
        position: absolute;
        bottom: 60px;
        z-index: 100;
        left: 50%;
        margin-left: -260px;
        width: calc(100% - 80px);
    }
    ul{
        display: flex;
        position:relative;
        z-index: 200;
            li{
                width:16.5%;
                .number{
                width:40px;
                height:40px;
                border-radius: 40px;
                text-align: center;
                color:$deepGray;
                border:3px solid $btnGray;
                margin:0 30px;
                line-height:36px;
                font-size:22px;
                font-weight:bold;
                box-sizing: border-box;
                background:#fff;
                 &.active{
                    border:2px solid $yellow;
                 }
                }
                p{
                color:$btnGray; 
                text-align: center;
                margin:10px 0;
                }
            }
    }
}


</style>