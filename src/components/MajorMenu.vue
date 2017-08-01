<template>
  <div class="major-menu">
    <ul>
      <li>
        <div class="major-menu-item">
          <img src="../assets/image/borrow_by_code.png"></img>
          <p>码上借</p>
        </div>
      </li>
      <li>
        <div class="major-menu-item">
          <img src="../assets/image/upload_book_icon.png"></img>
          <p>上传</p>
        </div>
      </li>
      <li>
        <div class="major-menu-item">
          <img src="../assets/image/return_by_code.png"></img>
          <p>码上还</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'majormenu',
  data () {
    return {
      msg: 'Welcome to majormenu'
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";
.major-menu{
  height: 14.54rem;
  padding-top: 1.81rem;

  li{
    width: 33.3%;
    float: left;

    .major-menu-item{
      position: relative;
      text-align: center;
      height: 9.09rem;
      width: 9.09rem;
      background-image: url(../assets/image/index_header_icon_bg.png);
      margin: 0 auto;
      background-size: 100% 100%;

      img{
        width: 4.54rem;
        height: 4.54rem;
        position: absolute;
        top: 1.81rem;
        left: 50%;
        margin-left: -2.27rem;
      }

      p{
        color: #fff;
        font-size: $normalFontSize;
        padding-top: 6.36rem;
      }
    }

  }
}
</style>
