<template>
  <div class="modal" v-if="mView">
    
    test
    <div class="close" @click="modalClose">닫기</div>
    <!-- <div class="close" @click="$emit('modalClose')">닫기</div> -->
  
  </div>
</template>

<script>
export default {
    props:[
        "mView"
    ],
    methods:{
        modalClose(){
            this.$emit("mClose")
        }
    }
}
</script>

<style>
.modal{
  width: 300px;height: 300px;
  background: pink;
  position: fixed;
  left: 50%;top: 50%;
  transform: translate(-50%,-50%);
}
</style>