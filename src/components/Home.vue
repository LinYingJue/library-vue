<template>
  <div class="home">
    <div class="bg-block">
      <searchbar v-on:toggleMenu="toggleMenu"></searchbar>
      <majormenu></majormenu>
    </div>
    <minormenu></minormenu>
    <guessyoulike></guessyoulike>
    <transition
      :name="transitionName"
      v-on:after-enter="toggleShadow"
      v-on:after-leave="toggleShadow">
      <drawermenu v-if="showMenu" v-on:toggleMenu="toggleMenu" class="child-view" key="menu"></drawermenu>
    </transition>
    <div class="shadow-bg" v-if="showShadow" v-on:click="toggleMenu" key="bg"></div>
  </div>
</template>

<script>
import searchbar from '@/components/SearchBar'
import majormenu from '@/components/MajorMenu'
import minormenu from '@/components/MinorMenu'
import drawermenu from '@/components/DrawerMenu'
import guessyoulike from '@/components/GuessYouLike'

export default {
  name: 'home',
  data () {
    return {
      transitionName: 'slide-left',
      showMenu: false,
      showShadow: false
    }
  },
  components: { searchbar, majormenu, minormenu, drawermenu, guessyoulike },
  methods: {
    toggleMenu: function () {
      this.showMenu = !this.showMenu
    },
    toggleShadow: function () {
      this.showShadow = !this.showShadow
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../assets/style/animate.css";
.bg-block{
  background-image: url(../assets/image/index_header_bg.png);
  background-size: 100% 100%;
}
.child-view{
  transition: all .5s ease;
}
.shadow-bg{
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #333;
  opacity: 0.5;
  top: 0;
  left: 0;
  z-index: 2;
}
.slide-left-enter-active, .slide-left-leave-active{
  -webkit-transform: translate(-17.04rem, 0);
  transform: translate(-17.04rem, 0);
}
</style>
