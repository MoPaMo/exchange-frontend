<template>
<div class="container">
  <h2>Exchange</h2>

  <new-crs/>
  <br/>
<searchjumbo msg="Finde dein Traumstück"/>
</div>
</template>

<script>
// @ is an alias to /src
import newCrs from '@/components/newCrs.vue'
import searchjumbo from '@/components/searchJumbo.vue'

export default {
  name: 'Home',
  components: {
    newCrs,
    searchjumbo
  }
}
</script>
