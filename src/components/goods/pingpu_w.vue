<template>
  <div id="pingpu_w">
    <div class="product_item" v-for="item in list" :key="item.id">
      <div class="product_cart">
        <router-link :to="{path: '/detail' , query: {goodsId: item.id}}" class="product_img" target="_blank">
          <div class="product_img_box">
            <img class="product_img_con" :src="item.smallPic">
          </div>
        </router-link>
        <div class="product_info">
          <div class="product_title">
            <router-link :to="{path: '/detail' , query: {goodsId: item.id}}" class="product_word"><span>{{item.goodsName}}</span></router-link>
          </div>
          <div class="product_price">{{item.priceShow}}元</div>
          <!-- <del class="product_price">{{item.price+5}}元</del> -->
        </div>
      </div>
    </div>
    <div class="shadow_line"></div>
  </div>
</template>
<script>
export default {
  name: 'pingpu_w',
  props: {
    list: {
      type: Array,
      default: () => []
    }
  },
  data () {
    return {}
  }
}

</script>
<style lang="scss" scoped>
body, div, span, header, footer, nav, section, aside, article, ul, dl, dt, dd, li, a, p, h1, h2, h3, h4, h5, h6, i, b, textarea, button, input, select, figure, figcaption {
  padding: 0;
  margin: 0;
  list-style: none;
  font-style: normal;
  text-decoration: none;
  border: none;
  font-family: "Microsoft Yahei";
  box-sizing: border-box;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-smoothing: antialiased;
  &:hover {
    outline: none;
  }
  &:focus {
    outline: none;
  }
}
input[type="button"], input[type="submit"], input[type="search"], input[type="reset"] {
  -webkit-appearance: none;
}
table, tr, td {
  border-spacing: 0;
}
textarea {
  -webkit-appearance: none;
}
  #pingpu_w {
    display: flex;
    flex-wrap: wrap;
    /* 修改这里可以公用一个组件 */
    width: 986px;
    border: 1px solid #dbe3ef;
  }
  .product_item {
    width: 25%;
    border-right: 1px solid #dbe3ef;
    padding: 18px 15px;
    text-align: center;
    overflow: hidden;
    &:nth-child(n) {
      border-bottom: 1px solid #dbe3ef;
    }
    &:nth-child(4n) {
      border-right: 1px solid transparent;
    }
    .product_cart {
      width: 160px;
      display: inline-block;
      vertical-align: top;
      font-size: 14px;
      line-height: 16px;
      text-align: left;
      .product_img {
        margin-bottom: 13px;
        display: block;
        .product_img_box {
          width: 100%;
          height: 100%;
          overflow: hidden;
          position: relative;
          .product_img_con {
            display: block;
            max-width: 100%;
            max-height: 100%;
          }
        }
      }
      .product_info {
        color: #666;
        overflow: hidden;
        width: 100%;
        .product_title {
          width: 100%;
          max-height: 38px;
          white-space: normal;
          line-height: 20px;
          word-break: break-all;
          overflow: hidden;
          text-overflow: ellipsis;
          -webkit-box-orient: vertical;
          display: -webkit-box;
          -webkit-line-clamp: 2;
          .product_word {
            color: #333;
            word-break: break-all;
            &:hover {
              color: #ef7026;
              text-decoration:underline;
            }
          }
        }
        .product_price {
          color: #333;
          font-weight: 700;
          margin-top: 5px;
          white-space: nowrap;
          overflow: hidden;
          text-overflow: ellipsis;
          text-align: center;
        }
      }
    }
  }
.shadow_line {
  position: absolute;
  bottom: 1px;
  height: 1px;
  background: #fff;
  width: 100%;
}
</style>
