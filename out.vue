<template>
  <div id="out">
      tuichu
      <button>按钮</button>

      <div>
        <button @click="selectFile">选择文件</button>
        <input type="file" id="oInput">
        <div class="odivBox">
            
            <img src="../assets/img/123.jpg" alt=""  class="inImg">
        </div>
        
        <!-- <el-input @input="oInput" v-model="valueInput"></el-input> -->
      </div>
      <!-- 组件传参 父子组件 $emit .sync -->
      <Comit :passData.sync="passData"  />
      <parentComponent  :name="name" :age="age" :intre="intre" @fromSon="fromSon" />
      <router-view></router-view>
      
  </div>
</template>

<script>
import {paintFixedWaterMark} from '../utils'
import Comit from"@/components/comit"
import parentComponent from "@/components/parentComponent"
console.log(paintFixedWaterMark)
export default {
    name:"out",
    data(){
        return {
            valueInput:"",
            passData:"123父组件传递",
            name:"李逵",
            age:23,
            intre:"抢劫",
            isShow:false
        }
    },
    components:{
        Comit,
        parentComponent
    },
    created(){
        console.log(this.name)
        this.$eventBus.$off("getData")
        this.$eventBus.$on('getData',function(e){
            console.log(e)
            this.name = e
            console.log(this.name)
            this.isShow = false
            this.isShow = true
        })
        
    },
    mounted(){
        // console.log(paintFixedWaterMark)
        let str = 20222343+' ' +'name'
        paintFixedWaterMark(str)
        let odivBox = document.getElementsByClassName('odivBox inImg')[0]
        // odivBox.addEventListener("mouseenter", function(){
        //     this.parentNode()
        // })
        // this.aa()
       
    },
    methods:{
        aa(){
            // console.log(paintFixedWaterMark)
        },
        selectFile(){
            console.log("选择文件")

            let a = document.getElementById('oInput')
            a.click()
            a.change=(e)=>{
                console.log

            }
           
            console.log(a.files)
        },
        oInput(){
            console.log(this.valueInput)
        },
        changeValue(e){
            console.log(e)
            this.passData = e

        },
        fromSon(e){
            this.name = e
           

        }
        
    
    }

}
</script>


<style>
#oInput{
    display: none;
    
}
.odivBox img{
    margin: 10px;
    width: 50px;

        
}

</style>