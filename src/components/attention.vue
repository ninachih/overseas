<template>
    <div id="attention">
        <div>線上投保注意事項 <img src="../assets/attention.svg" alt=""></div>
    </div>
</template>
<script>
export default {
  name: "attention",
}
</script>
<style lang="scss">
#attention{
    width:100%;
    text-align: center;
    color:#fff;
    padding:0 35px;
    box-sizing: border-box;
    font-weight:bold;
    background:$mainBlue;
    line-height:50px;
    border-radius: 27px;
    img{
        display:block;
        float:right;
        margin-top:11px;
        cursor: pointer;
    }
}


</style>