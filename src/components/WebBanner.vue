<template>
  <div class="container">
    <ul>
      <li v-for="item in banData" :key="item">
        <img :src="`./images/directs/${item.src}`" alt="">
        <div class="txt">
          {{item.name}}  
        </div>
        
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props:[
    "banData"
  ]
}
</script>

<style lang="scss" scoped>
  .container{
    width: 1200px;
    margin: 0 auto;
    ul{
      display: flex;
     .txt{
      text-align: center;
     }
    }
    img{
      display: block;
      width: 100%;
    }
  }

</style>