<template>
<div class="bg-light p-5 mb-4 rounded">
  <div v-if="loading" class="placeholder-glow"> 
    <span class="placeholder col-6"></span> <br />
    <span class="placeholder col-3"></span><br />
    <span class="placeholder col-6"></span>
  </div>
  <div v-if="!loading">
    Actual content
  </div>
</div>
</template>

<script>
export default {
  name: 'item-desc',
  props: {},
  data() {
    return {
      loading:true,
      newItems: [{
        name: "Blaue Weste",
        id: "afnzu"
      }, "b"]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
