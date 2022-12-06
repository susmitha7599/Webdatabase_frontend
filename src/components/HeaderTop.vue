<template>
  <div>
    <h1>{{appName}}</h1>
    <h4>{{tagName}}</h4>
  </div>
</template>
<script>
export default{
  name:'HeaderTop',
  props:{
    appName:String,
    tagName:String
  }
}
</script>
<style scoped>
div{
        text-align: center;
        border: 0.3em solid black;
        background-color: #AB6B51;
        font-weight: bold;
        font-style: italic;
    }
</style>