<template>
  <div class="minor-menu">
    <ul>
      <li>
        <div class="minor-menu-item">
          <img src="../assets/image/all_icon.png"></img>
          <p>所有</p>
        </div>
      </li>
      <li>
        <div class="minor-menu-item">
          <img src="../assets/image/rank_icon.png"></img>
          <p>排行</p>
        </div>
      </li>
      <li>
        <div class="minor-menu-item">
          <img src="../assets/image/borrow_icon.png"></img>
          <p>借阅</p>
        </div>
      </li>
      <li>
        <div class="minor-menu-item">
          <img src="../assets/image/exchange_icon.png"></img>
          <p>圈子</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'minormenu',
  data () {
    return {
      msg: 'Welcome to minormenu'
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";
.minor-menu{
  height: 10.9rem;
  width: 100%;
  text-align: center;
  padding:2.27rem 1.81rem 0 1.81rem;
  border-bottom: 0.18rem solid #d3d3d3;
  box-sizing: border-box;

  li{
    width: 25%;
    float: left;

    img{
      width: 3.63rem;
      height: 3.63rem;
    }

    p{
      color: #565656;
      font-size: $normalFontSize;
      margin: 0;
    }
  }
}
</style>
