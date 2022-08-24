<template>
  <div class="total">
    <Header></Header>
    <div class="article">
      <div class="recom">
        <ul>
          <li class="active">推荐</li>
          <li>最新</li>
          <li>热榜</li>
        </ul>
      </div>
      <div class="container-left-middle">
        <div class="container-left-middle-1" v-for="item in this.ArticleData" :key="item.id" @click="goToArticle(item.id)">
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
  </div>
</template>

<script>
import Adivertising from '../components/Adivertising.vue'
import Header from '../components/Header.vue'
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
    Header
  },
  methods: {
    ImgSrc(ImgSrc) {
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
        objKey++
        this.ArticleData = this.ArticleData.concat(obj[objKey])
      }
    },

    goToArticle(id) {
      id = id - 1
      this.$router.push({ path: '/article/' + id })
    }
  },
  mounted() {
    window.addEventListener('scroll', this.scrollFn)
    if (this.$store.state.database.length <= 15) {
      this.ArticleData = this.$store.state.database
    } else {
      for (let i = 0; i < this.$store.state.database.length / 15; i++) {
        obj[i] = this.$store.state.database.slice(15 * i, 15 * (i + 1))
      }
      this.ArticleData = obj[0]
    }
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
  .article {
    width: 700px;
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
      cursor: pointer;
      ul {
        display: flex;
        padding-left: 10px;
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
      .div1 {
        padding-left: 10px;
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
    .container-left-middle-1:hover {
      background-color: rgb(248, 248, 248);
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
