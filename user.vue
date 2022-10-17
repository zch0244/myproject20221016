<template>
  <div id="user">
      userImport
      <span>{{user}}</span>
      <span @click="busBtn">bus按钮</span>
  </div>
</template>

<script>
export default {
    name:"userImport",
    data(){
      return {
        user:"我是User"
      }
    },
    methods:{
      busBtn(){
        this.$eventBus.$emit("getData",this.user)
        this.$router.push("/out")
      }
    }

}
</script>

<style>

</style>