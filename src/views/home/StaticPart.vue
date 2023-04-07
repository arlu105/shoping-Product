<template>
  <div class="position">
    <span class="iconfont position__icon">&#xe64c;</span>
    西安工业大学未央校区学生服务中心
    <span class="iconfont position__notice">&#xe60d;</span>
  </div>
  <div class="search">
    <span class="iconfont">&#xe600;</span>
    <input class="search__text" type="text" placeholder="山姆大叔的商店" />
  </div>
  <div class="banner">
    <img
      class="banner__img"
      src="http://www.dell-lee.com/imgs/vue3/banner.jpg"
    />
  </div>
  <div class="icons">
    <div class="icons__item"
    v-for="item in iconList"
    :key='item.desc'>
      <img
        class="icons__item__img"
        :src="`http://www.dell-lee.com/imgs/vue3/${item.imgName}.png`"
      />
      <p class="icons__item__desc">{{item.desc}}</p>
    </div>
  </div>
  <div class="gap"></div>
</template>

<script>
export default {
  name: 'StaticPart',
  setup () {
    const iconList = [
      { imgName: '超市', desc: '超市便利' },
      { imgName: '菜市场', desc: '菜市场' },
      { imgName: '水果店', desc: '水果店' },
      { imgName: '鲜花', desc: '鲜花绿植' },
      { imgName: '医药健康', desc: '医药健康' },
      { imgName: '家居', desc: '家居时尚' },
      { imgName: '蛋糕', desc: '烘焙蛋糕' },
      { imgName: '签到', desc: '签到' },
      { imgName: '大牌免运', desc: '大牌免运' },
      { imgName: '红包', desc: '红包套餐' }
    ]
    return { iconList }
  }
}
</script>

<style lang="scss" scoped>
@import "../../style/viriables.scss";
@import "../../style/mixins.scss";
.position {
  color: $content-fontcolor;
  position: relative;
  padding: 0.16rem 0.23rem 0.24rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipsis;
  .position__icon {
    position: relative;
    top: 0.01rem;
    // margin-right: 0.08rem;
    font-size: 0.2rem;
  }
  .position__notice {
    position: absolute;
    font-size: 0.2rem;
    right: 0;
    top: 0.17rem;
  }
}

.search {
  margin-bottom: 0.12rem;
  height: 0.32rem;
  line-height: 0.32rem;
  background: $search-bgColor;
  color: $search-fontColor;
  border-radius: 0.16rem;
  font-size: 0.14rem;
  .iconfont {
    font-size: 0.2rem;
    display: inline-block;
    position: relative;
    padding: 0 0.12rem 0 0.16rem;
  }
  &__text {
    border: none;
    background:$search-bgColor;
    outline: none;
  }
}

.banner {
  height: 0;
  overflow: hidden;
  padding-bottom: 25.4%;
  &__img {
    width: 100%;
  }
}

.icons {
  margin-top: 0.16rem;
  display: flex;
  flex-wrap: wrap;
  &__item {
    width: 20%;
    &__img {
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &__desc {
      text-align: center;
      margin: 0.06rem 0 0.16rem 0;
      color: $content-fontcolor;
    }
  }
}

.gap {
  margin: 0 -0.18rem;
  height: 0.1rem;
  background: $content-bgColor;
}
</style>
