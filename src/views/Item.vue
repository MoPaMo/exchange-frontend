<template>
<div class="container">
  <div class="row">
    <div class="col-md card" style="width: 100%">
      <img src="placeholder.jpg" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">{{item.name}}</h5>
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        <button class="btn btn-primary">Interesse</button>
      </div>
    </div>
    <div class="col-md">
      <item-desc />
    </div>
  </div>
</div>
</template>

<script>
import itemDesc from '@/components/description.vue'

export default {
  name: 'Item',
  components: {
    itemDesc
  },
  data() {
    return {
      item: {
        name: "test"
      }
    }
  },
  methods:{
    update(n){
      console.log(n.params.id);

    }
  },
  mounted() {
    this.update(this.$route.params.id)
  },
  watch: {
    $route(to, from) {
      this.update(from);
    }
  }
}
</script>
