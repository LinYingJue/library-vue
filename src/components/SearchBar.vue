<template>
  <div>
    <img class="menu-icon" src="../assets/image/menu_icon.png" v-on:click="showMenu()"></img>
    <p>
      <img class="search-icon" src="../assets/image/search_icon.png"></img>
      <input type="text"></input>
    </p>
  </div>
</template>

<script>
export default {
  name: 'searchbar',
  data () {
    return {
      msg: 'Welcome to searchbar'
    }
  },
  methods: {
    showMenu: function () {
      this.$emit('toggleMenu')
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";
div {
  height: 4.5rem;
  position: relative;

  .menu-icon{
    position: absolute;
    width: 2.2rem;
    top: 1.3rem;
    left: 1.3rem;
  }

  p{
    position: relative;
    top: 0.9rem;
    margin: 0 1.3rem 0 5rem;
    width: auto;
    background-color: #30477b;
    border-radius: 6px;
    height: 2.7rem;

    .search-icon{
      height: 1.8rem;
      width: 1.6rem;
      position: absolute;
      top: 0.45rem;
      left: 0.45rem;
    }

    input{
      outline: none;
      height: 2.7rem;
      border: none;
      background-color: #586780;
      padding-left: 2.7rem;
      line-height: 2.7rem;
      width: 100%;
      border-radius: 6px;
      color: #fff;
      box-sizing: border-box;
      font-size: $normalFontSize;
    }
  }
}
</style>
