<template>
<div class="">
  <div v-if="loading" class="placeholder-glow">
    <span class="placeholder col-6"></span> <br />
    <span class="placeholder col-3"></span><br />
    <span class="placeholder col-6"></span>
  </div>
  <div v-if="!loading">
    <div>{{name}}</div>
    <div class="small text-muted"><span>Seit {{date}} auf Exchange</span> · <span>{{item_count}} Stücke online</span></div>
  </div>
</div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'userinfo',
  props: {},
  data() {
    return {
      loading: true,
      name: "John Doe",
      date: "3w",
      item_count: "15"
    }
  },
  created() {
    axios.get("/api/user.txt", {params:{id:"123"}}).then((res)=>{
      this.loading = false;
      let data=JSON.parse(res);
      this.name=data.name;
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
