<template>
  <div>
    <img class="back-icon" src="../assets/image/arrow-left.png" v-on:click="goBack()"></img>
    <p>{{ title }}</p>
  </div>
</template>

<script>
export default {
  name: 'titleBar',
  props: [ 'title' ],
  methods: {
    goBack: function () {
      this.$router.go(-1)
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";
div {
  height: 4.5rem;
  position: relative;
  background-image: url(../assets/image/index_header_bg.png);

  .back-icon{
    position: absolute;
    top: 1.27rem;
    left: 0.9rem;
    width: 1.54rem;
  }

  p{
    text-align: center;
    font-size: $titleFontSize;
    margin: 0;
    color: #fff;
    height: 4.5rem;
    line-height: 4.5rem;
  }
}
</style>
