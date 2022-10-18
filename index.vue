<template>
  <div id="HelloWorld">
      <van-tabs v-model="activeTitle">
        <van-tab title="标签 1">内容 1</van-tab>
        <van-tab title="标签 2">内容 2</van-tab>
        <van-tab title="标签 3">内容 3</van-tab>
        <van-tab title="标签 4">内容 4</van-tab>
      </van-tabs>
      <span class="textCss">我的</span>
      <van-tabbar v-model="active">
        <van-tabbar-item icon="home-o">标签</van-tabbar-item>
        <van-tabbar-item icon="search">标签</van-tabbar-item>
        <van-tabbar-item icon="friends-o">标签</van-tabbar-item>
        <van-tabbar-item icon="setting-o">标签</van-tabbar-item>
      </van-tabbar>
      <div class="QrImg" >
        <span>123</span>
        
      </div>
  </div>
</template>

<script>
let QRCode = require('qrcode') 
// import qrcode from '../utils/qrcode'
// import QRCode from 'qrcode'; 
export default {
    name:"HelloWorld",
    data(){
      return{
        active:0,
        activeTitle:0,
        src:""
      }
    },
    mounted(){
      // qrcode('http://www.baidu.com')
    
    // let qrcode = new QRCode('qrcode', { //这里‘qrcode’是dom对象，也可以是this.$refs.qrcode150, //图像宽度
    //     height: 150, //图像高度
    //     colorDark : "#000000", //前景色
    //     colorLight : "#ffffff", //背景色
    //     typeNumber:4, 
    //     // correctLevel : QRCode.CorrectLevel.H //容错级别 容错级别有：（1）QRCode.CorrectLevel.L （2）QRCode.CorrectLevel.M （3）QRCode.CorrectLevel.Q （4）QRCode.CorrectLevel.H
    // })
    // console.log(qrcode)

      // let url = qrcode.toDataURL('http://www.baidu.com')
      
      // console.log(11111,'----',url)
    }
}
</script>

<style scoped>
.qrImg{
  width: 100px;
  height: 100px;
}

.QrImg{
  width:100px;
  height:100px;
  border:1px solid red;
}
.textCss{
  font-size: 12px;
}

</style>
