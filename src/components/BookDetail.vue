<template>
  <div>
    <titlebar :title="this.title"></titlebar>
    <div class="book-detail-img">
      <img class="book-pic" src="../assets/image/book_sample.png"></img>
      <img class="book-status-pic" src="../assets/image/borrowable_icon.png"></img>
    </div>
    <div class="book-detail-info">
      <p class="book-title">囧的故事</p>
      <p class="book-owner">都比哥
        <span>
          <img class="like-icon" src="../assets/image/like_icon.png"></img>
          <font>0</font>
          <img class="borrow-icon" src="../assets/image/borrow_icon.png"></img>
          <font>0</font>
        </span>
      </p>
      <p class="book-desc">
        该书暂无简介
      </p>
    </div>
  </div>
</template>

<script>
import titlebar from '@/components/TitleBar'

export default {
  name: 'bookdetail',
  data () {
    return {
      msg: 'Welcome to bookDetail',
      title: '图书详情'
    }
  },
  components: { titlebar }
}
</script>

<style lang="scss">
@import "../assets/style/common.scss";

.book-detail-img{
  position: relative;
  background: #fff;
  .book-pic{
    display: block;
    margin: 0 auto;
    padding-top: 0.18rem;
    max-width: 100%;
  }
  .book-status-pic{
    position: absolute;
    bottom: 0.9rem;
    right: 0.9rem;
    width: 4.54rem;
    z-index: 8000;
  }
}

.book-detail-info{
  padding-left: .9rem;
  padding-right: .9rem;
  background: #fff;
  .book-title{
    word-wrap: break-word;
    margin: 0;
    font-size: 1.63rem;
    font-weight: bold;
    padding-left: .9rem;
    padding-top: 1.81rem;
  }
  .book-owner{
    font-size: 1.09rem;
    color: #8d8d8d;
    padding-left: .9rem;
    margin: 0;
    height: 2.9rem;
    line-height: 2.9rem;
    text-align: left;
    span{
      color: #888;
      padding-right: .9rem;
      float: right;
      height: 2.9rem;
      line-height: 2.9rem;
      img{
        vertical-align: text-bottom;
      }
      .like-icon{
        width: 1.45rem;
      }
      .borrow-icon{
        width: 1.63rem;
        margin-left: .45rem;
      }
    }
  }
  .book-desc{
    min-height: 4.54rem;
    font-size: $normalFontSize;
    margin: 1.81rem 0 0 0;
    padding-left: .9rem;
    padding-right: .9rem;
    text-align: justify;
  }
}
</style>
