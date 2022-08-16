<template>
  <div class="total">
    <header>
      <ul>
        <li class="active">综合</li>
        <li>后端</li>
        <li>前端</li>
        <li>Android</li>
        <li>ios</li>
        <li>人工智能</li>
        <li>开发工具</li>
        <li>代码人生</li>
        <li>阅读</li>
      </ul>
    </header>
    <div class="article">
      <div class="recom">
        <ul>
          <li class="active">推荐</li>
          <li>最新</li>
          <li>热榜</li>
        </ul>
      </div>
      <div class="container-left-middle">
        <div class="container-left-middle-1" v-for="item in this.ArticleData" :key="item.id">
          <ul>
            <li>{{ item.name }}</li>
            <li>|</li>
            <li>{{ item.day }}天前</li>
            <li>|</li>
            <li>{{ item.category }}</li>
          </ul>
          <div class="div1">
            <br />
            <span
              ><h3>{{ item.title }}</h3></span
            >
            <div class="span">
              <span>{{ item.intro }}</span>
            </div>
            <div></div>
            <img class="img1" :src="item.imgsrc" />
          </div>
        </div>
      </div>
    </div>
    <img class="advs" src="../assets/image/advs.png" alt="" />
    <img class="advs2" src="../assets/image/advs2.png" alt="" />
    <Database @emitData="getData"></Database>
  </div>
</template>

<script>
import Adivertising from '../components/Adivertising.vue'
import Database from '../components/Database.vue'
let obj = {}
let objKey = 0
export default {
  name: 'home',
  data() {
    return {
      ArticleData: {}
    }
  },
  components: {
    Adivertising,
    Database
  },
  methods: {
    getData(val) {
      if (val.length <= 15) {
        this.ArticleData = val
      } else {
        for (let i = 0; i < val.length / 15; i++) {
          obj[i] = val.slice(15 * i, 15 * (i + 1))
        }
        this.ArticleData = obj[0]
      }
    },
    getImgSrc(ImgSrc) {
      return require(ImgSrc)
    },
    scrollFn() {
      let windowHeight = window.innerHeight || document.documentElement.clientHeight
      let st = window.pageYOffset || document.documentElement.scrollTop
      let scrollHeight = document.documentElement.scrollHeight
      if (objKey === Object.keys(obj).length - 1) {
        return
      }
      if (windowHeight + st >= scrollHeight) {
        console.log(Object.keys(obj).length)
        objKey++
        this.ArticleData = this.ArticleData.concat(obj[objKey])
      }
    }
  },
  mounted() {
    window.addEventListener('scroll', this.scrollFn)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.scrollFn)
  }
}
</script>

<style lang="less" scoped>
@import '../total.less';
.total {
  background-color: rgb(246, 246, 246);
  header {
    background-color: #fff;
    border-bottom: 1px solid #f1f1f1;
    width: 100%;
    height: 46px;
    ul {
      font-size: 14px;
      display: flex;
      align-items: center;
      line-height: 46px;
      color: gray;
      li:nth-child(1) {
        margin-left: 370px;
      }
      li {
        margin-right: 25px;
        cursor: pointer;
        &.active {
          color: #1e80ff;
        }
      }
      li:hover {
        color: #1e80ff;
      }
    }
  }
  .article {
    width: 700px;
    height: 2000px; //暂定
    background-color: #fff;
    margin-left: 370px;
    margin-top: 10px;
    .recom {
      height: 46px;
      color: grey;
      font-size: 14px;
      line-height: 46px;
      border-bottom: 1px solid #f1f1f1;
      ul {
        display: flex;
        align-items: center;
        li:nth-child(1) {
          margin-left: 25px;
        }
        li {
          width: 55px;
          cursor: pointer;
          &.active {
            color: #1e80ff;
          }
        }
        li:hover {
          color: #1e80ff;
        }
      }
    }
    .container-left-middle-1 {
      margin-left: 10px;
      ul {
        display: flex;
        li {
          margin-top: 15px;
          font-size: 13px;
          margin-right: 10px;
        }
        li:nth-child(1) {
          color: rgb(80, 80, 80);
          border-right: 1px solid #ccc;
        }
        li:nth-of-type(n + 2) {
          color: grey;
        }
      }
      .shu {
        margin-left: 5px;
      }

      .img1 {
        float: right;
        width: 120px;
        margin-right: 20px;
        height: 80px;
        margin-top: -100px;
      }

      h3 {
        font-size: 16px;
        padding-bottom: 20px;
        margin-top: 8px;
        font-weight: bold;
        color: black;
      }

      .span {
        padding-bottom: 20px;
        font-size: 15px;
        width: 550px;
        border-bottom: 1px solid gainsboro;
        font-family: Arial, Helvetica, sans-serif;
        color: #86909c;
      }
    }
  }
  .advs,
  .advs2 {
    cursor: pointer;
    width: 240px;
    position: absolute;
    left: 1087px;
    &.advs {
      top: 115px;
    }
    &.advs2 {
      top: 740px;
    }
  }
}
</style>
