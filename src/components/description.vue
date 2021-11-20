<template>
<div class="bg-light p-5 mb-4 rounded">
  <div v-if="loading" class="placeholder-glow">
    <span class="placeholder col-6"></span> <br />
    <span class="placeholder col-3"></span><br />
    <span class="placeholder col-6"></span>
  </div>
  <div v-if="!loading">
    <userinfo />
    {{text}}


  </div>
</div>
</template>

<script>
import userinfo from '@/components/userinfo.vue'

export default {
  name: 'item-desc',
  components:{userinfo},
  props: {},
  data() {
    return {
      loading: true,
      text:""
    }
  },
  watch:{
    text:(val)=>{
      if(val)
      this.loading=false;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
