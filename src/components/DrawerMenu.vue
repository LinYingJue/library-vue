<template>
  <div class="drawer-menu">
    <img src="../assets/image/user_header_icon.png"></img>
    <ul>
      <li><p>我的图书</p></li>
      <li><p>借阅记录</p></li>
      <li><p>我的积分</p></li>
      <li><p>关于</p></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'drawermenu',
  data () {
    return {
      msg: 'Welcome to searchbar'
    }
  },
  methods: {
    hideMenu: function () {
      this.$emit('toggleMenu')
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";
.drawer-menu{
  background-color: #444;
  width: 17.04rem;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 3;
  color: #fff;
  text-align: center;

  img{
    height: 6.36rem;
    width: 6.36rem;
    margin-top: 9.09rem;
    border-radius: 6.36rem;
  }

  ul{
    margin-top: 2.72rem;

    li{
      border-bottom: 0.09rem solid #fff;
      margin-left: 2.72rem;
      margin-right: 2.72rem;

      p{
        height: 4.54rem;
        margin: 0;
        line-height: 4.54rem;
        font-size: 1.45rem;
      }
    }
  }
}
</style>
