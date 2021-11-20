<template>
<div class="bg-light p-5 mb-4 rounded">
  <h2 class="display-6 fw-bold">{{msg}}</h2>
  <form class="input-group mb-3" @submit="sub">
    <input required type="search" class="form-control" v-model="input" placeholder="Gib etwas ein" aria-label="Suchfeld" aria-describedby="button-addon2">
    <input class="btn btn-outline-secondary" type="submit" value="Suchen" id="button-addon2"/>
  </form>
</div>
</template>

<script>
//search jumbotron
export default {
  name: 'searchjumbo',
  props: ["msg"],
  data(){
    return{
      input:""
    }
  },
  methods:{
    sub(e){
      e.preventDefault();
      this.$router.push("search/"+this.input)
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
