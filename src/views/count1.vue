<template>
  <div id="winnerList">
    <goTop/>
    <div class="winnerKv">
    <h2>得獎名單</h2>
    </div>  
    
    <div class="content">
     
    </div>
  </div>
</template>
<script>
import goTop from "@/components/gotop.vue";
export default {
  name: "winnerList",
  components:{
    goTop,
  }
};
</script>