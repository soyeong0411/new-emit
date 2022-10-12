<template>
  <web-banner
    v-bind:banData="banData"
    @click="modalView=true"
  ></web-banner>
  <web-modal :mView="modalView" @mClose="modalClose"></web-modal>
  <!-- <web-modal :mView="modalView" @modalClose="modalView=false"></web-modal> -->
  {{modalView}}
  
  
</template>

<script>
import WebBanner from "@/components/WebBanner.vue"
import banData from "@/data/directs.js"
import "@/assets/style.css"
import WebModal from "@/components/WebModal.vue"


export default {
  components:{
    WebBanner,
    WebModal,
  },
  data(){
    return {
      banData:banData,
      modalView:false,  // 오브젝트데이터
    }
  },
  methods:{
    modalClose(){
      this.modalView=false  // 스크립트 영역
    }
  }
}
</script>

<style>
/* @import url(./assets/style.css); */

</style>