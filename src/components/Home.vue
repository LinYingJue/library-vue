<template>
  <div class="home">
    <div class="bg-block">
      <searchbar></searchbar>
      <majormenu></majormenu>
    </div>
    <minormenu></minormenu>
  </div>
</template>

<script>
import searchbar from '@/components/SearchBar'
import majormenu from '@/components/MajorMenu'
import minormenu from '@/components/MinorMenu'

export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: { searchbar, majormenu, minormenu }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.bg-block{
  background-image: url(../assets/image/index_header_bg.png);
  background-size: 100% 100%;
}
</style>
