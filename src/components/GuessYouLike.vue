<template>
  <div>
    <p class="title">猜你喜欢</p>
    <ul>
      <li>
        <p class="owner">坑逼</p>
        <img src="../assets/image/book_sample.png"></img>
        <p class="book-name">Java指南</p>
      </li>
      <li>
        <p class="owner">坑逼</p>
        <img src="../assets/image/book_sample_1.png"></img>
        <p class="book-name">Java指南</p>
      </li>
      <li>
        <p class="owner">坑逼</p>
        <img src="../assets/image/book_sample.png"></img>
        <p class="book-name">Java指南</p>
      </li>
      <li>
        <p class="owner">坑逼</p>
        <img src="../assets/image/book_sample_1.png"></img>
        <p class="book-name">Java指南</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'guessyoulike'
}
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";

.title{
  font-size: $titleFontSize;
  margin: 0.9rem 0;
}
ul{
  width: 100%;
}
li{
  float: left;
  width: 25%;
  text-align: center;
  img{
    height: 9.09rem;
    width: 7.27rem;
  }
  p{
    margin: 0;
  }
  .owner{
    font-size: 1.09rem;
  }
  .book-name{
    font-size: $normalFontSize;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
  }
}
</style>
