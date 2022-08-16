<template>
  <nav>
    <div class="container">
      <img src="https://lf3-cdn-tos.bytescm.com/obj/static/xitu_juejin_web/e08da34488b114bd4c665ba2fa520a31.svg" />
      <ul>
        <li @click="$router.push('/home')" :class="$route.path === '/home' ? 'active' : ''">首页</li>
        <li @click="$router.push('/hot')" :class="$route.path === '/hot' ? 'active' : ''">沸点</li>
        <li @click="$router.push('/course')" :class="$route.path === '/course' ? 'active' : ''">课程</li>
        <li @click="$router.push('/show')" :class="$route.path === '/show' ? 'active' : ''">直播</li>
        <li @click="$router.push('/activity')" :class="$route.path === '/activity' ? 'active' : ''">活动</li>
        <li><a href="https://detail.youzan.com/show/goods/newest?kdt_id=104340304">商城</a></li>
        <li><a href="https://juejin.cn/app?utm_source=jj_nav">APP</a></li>
        <li><a href="https://juejin.cn/extension?utm_source=jj_nav">插件</a></li>
      </ul>
      <div class="search">
        <input type="text" placeholder="探索稀土掘金" />
        <div class="search_image"><img src="https://lf3-cdn-tos.bytescm.com/obj/static/xitu_juejin_web/1e8ab9a22f0ddc36349f60b38900d0bd.svg" /></div>
      </div>
      <div class="creator">
        <button>创作者中心</button>
        <div class="content"></div>
      </div>
      <div class="vip">
        <img src="https://lf3-cdn-tos.bytescm.com/obj/static/xitu_juejin_web/24127194d5b158d7eaf8f09a256c5d01.svg" alt="" />
        <span>会员</span>
      </div>
      <img class="bell" src="../assets/image/bell.png" alt="" />
      <img class="login" src="../assets/image/login.png" alt="" />
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    jumpFn() {
      this.$router.push()
    }
  }
}
</script>

<style lang="less" scoped>
@import '../total.less';
nav {
  border-bottom: 1px solid #f1f1f1;
  .container {
    width: 1440px;
    height: 60px;
    margin: auto;
    display: flex;
    align-items: center;
    img {
      cursor: pointer;
      width: 107px;
      height: 22px;
      margin-left: 15px;
      margin-right: 12px;
    }
    ul {
      cursor: pointer;
      width: 420px;
      display: flex;
      justify-content: space-around;
      align-items: center;
      color: #494848;
      font-size: 14px;
      margin-top: 1px;
      margin-right: 150px;
      li {
        height: 60px;
        border: 2px solid transparent;
        line-height: 60px;
        &.active {
          color: #1e80ff;
        }
        a {
          text-decoration: none;
          color: #494848;
        }
        a:hover {
          color: rgb(40, 40, 40);
        }
      }
      li:nth-child(-n + 5):hover {
        color: rgb(40, 40, 40);
        border-bottom: 2px solid #1e80ff;
      }
    }
    .search {
      width: 360px;
      height: 35.3px;
      border: 1px solid #c2c8d1;
      display: flex;
      align-items: center;
      margin-right: 25px;
      input {
        height: 35.3px;
        width: 315px;
        border: 0;
        padding: 0;
        outline: none;
        padding-left: 10px;
      }
      .search_image {
        cursor: pointer;
        height: 30px;
        width: 44px;
        background-color: rgb(238, 238, 238);
        border-radius: 10%;
        img {
          height: 17px;
          width: 17px;
          padding: 0;
          padding-left: 13px;
          padding-top: 6px;
          margin: 0;
        }
      }
    }
    .creator {
      width: 115px;
      height: 36px;
      background-color: #1e80ff;
      border-radius: 8%;
      flex-shrink: 0;
      cursor: pointer;
      button {
        height: 36px;
        width: 100px;
        color: white;
        background-color: #1e80ff;
        border: 0;
        border-right: 1px solid rgb(154, 154, 255);
        border-radius: 8%;
      }
      .content {
        width: 0px;
        height: 0px;
        border: 6px;
        border-style: solid;
        border-color: white transparent transparent;
        display: inline-block;
        position: relative;
        top: 3px;
      }
    }
    .vip {
      cursor: pointer;
      color: gray;
      font-size: 13px;
      img {
        width: 30px;
        margin-right: 0;
        margin-left: 20px;
      }
      span {
        width: 30px;
        position: relative;
        bottom: 5px;
      }
    }
    .bell {
      height: 24px;
      width: 20px;
    }
    .login {
      height: 40px;
      width: 70px;
    }
  }
}
</style>
