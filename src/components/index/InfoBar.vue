<template>
<div class="info-bar">
  <div class="infobar-item"><span>@余赊</span></div>
  <div class="infobar-item"><span>vuecli4.0.4实现抖音</span></div>
  <div class="infobar-item music-item">
    <span class="iconfont icon-yinfu"></span>
    <div class="music-name">
      <span data-text="此处应有掌声">此处应有掌声</span>
    </div>
   </div>
</div>
</template>

<script>
export default {
  name: "InfoBar"
}
</script>

<style scoped>
.info-bar{
  color: #ffffff;
  font-size: 16px;
  padding-left: 10px;
}
.info-bar .infobar-item {
  padding: 5px 0;

}
.infobar-item .icon-yinfu {
  margin-right: 5px;
}
.music-item {
 display: flex;

}
.music-item .music-name{
  width: 150px;
  white-space: nowrap;
  overflow: hidden;
  font-size: 14px;
}
.music-item .music-name span{
  display: inline-block;
  animation: scroll 5s linear infinite;
}
.music-item .music-name span::after{
  content: attr(data-text);
  margin-left: 30px;
}
 @keyframes scroll {
   from {
     transform: translateX(0);
   }
   to{
     transform: translateX(calc(-50% - 20px));

   }
 }


</style>
