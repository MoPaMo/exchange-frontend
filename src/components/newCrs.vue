<template>
<div class="bg-dark text-light p-5 mb-4 rounded">
  <h2 class="display-6 fw-bold">Neueste Stücke</h2>
  <div id="carouselExampleIndicators" class="carousel slide pt-3 rounded" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div :class="'ml-5 mr-5 carousel-item' +(i==0?' active':'')" v-for="item,i in newItems" :key="i">
        <div class="d-block container-fluid rounded v-100" style="background-image:url(placeholder.jpg); height:65vh;">
          <div class="carousel-caption ">
            <h5>{{item.name}} <span class="badge bg-secondary">L</span></h5>
            <router-link :to="'/item/'+item.id" class="btn btn-primary m-2  stretched-link">Ansehen</router-link>
          </div>
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</div>
</template>

<script>
export default {
  name: 'new-crs',
  props: {},
  data() {
    return {
      newItems: [{name:"Blaue Weste", id:"afnzu"}, "b"]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.crs-footer {
  background-color: #0006;
  padding: 2px;
  border-radius: 2px;
}
</style>
