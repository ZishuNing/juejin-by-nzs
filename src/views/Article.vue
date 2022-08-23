<template>
  <div class="total">
    <img src="../assets/image/sideOption.png" class="sideOption" />
    <mavonEditor class="article" v-model="content" defaultOpen="preview" :toolbarsFlag="false" :subfield="false" :navigation="true" :ishljs="false" />
    <div class="toc-fixed">
      <div class="toc">
        <div class="title">{{ this.directoryTitle }}</div>
        <div v-for="(item, index) in toc" :key="index">
          <a @click="scrollToPosition(item.href)">{{ item.name }}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mavonEditor } from 'mavon-editor'
import 'mavon-editor/dist/css/index.css'
import '../total.less'
import $ from 'jquery'

export default {
  components: { mavonEditor },
  data() {
    return {
      directoryTitle: '目录',
      toc: [],
      content: ''
    }
  },
  methods: {
    highlight() {
      var codehl = document.getElementsByTagName('code')
      if (location.href.indexOf('#reloaded') == -1) {
        location.href = location.href + '#reloaded'
        location.reload()
      }
      this.$nextTick(function () {
        for (let i = 0, len = codehl.length; i < len; i++) {
          codehl[i].setAttribute('class', 'prettyprint')
        }
      })
    },
    directoryClear() {
      let directory = document.getElementsByClassName('v-note-navigation-wrapper')
      directory[0].style.display = 'none'
    },
    getDirectoryContent() {
      let directoryTitle = document.getElementsByClassName('v-note-navigation-title')
      this.directoryTitle = directoryTitle[0].textContent
      this.$nextTick(() => {
        const aArr = $('a').toArray()
        let toc = []
        let flag = true
        aArr.forEach(item => {
          let href = $(item).attr('id')
          let name = $(item).parent().text()
          if (href) {
            for (let i = 0, len = toc.length; i < len; i++) {
              if (toc[i].href == '#' + href) {
                flag = false
              }
            }
            if (flag) {
              toc.push({
                href: '#' + href,
                name
              })
            }
          }
        })
        this.toc = toc
      })
    },
    scrollToPosition(id) {
      let position = $(id).offset()
      position.top -= 80
      $('html,body').animate({ scrollTop: position.top }, 1000)
    }
  },
  created() {
    this.content = this.$store.state.database[this.$route.params.id].content
  },
  mounted() {
    this.highlight()
    this.directoryClear()
    this.getDirectoryContent()
  }
}
</script>

<style lang="less" scoped>
.total {
  background-color: rgb(246, 246, 246);
  .sideOption {
    cursor: pointer;
    width: 73px;
    position: absolute;
    top: 130px;
    left: 175px;
  }
  .article {
    width: 820px;
    background-color: #fff;
    margin-left: 270px;
    position: relative;
    top: 20px;
  }
}
.toc-fixed {
  position: fixed;
  width: 270px;
  right: 260px;
  top: 80px;
  background-color: #fff;
  padding: 20px 20px 0 20px;
  border-radius: 3%;
  font-family: 'Arial', 'Microsoft YaHei', '黑体', '宋体', sans-serif;
  .toc {
    width: 100%;
    overflow-y: auto;
    word-break: break-all;
    .title {
      font-weight: 500;
      font-size: 16px;
      margin-bottom: 15px;
      padding-bottom: 10px;
      border-bottom: 1px solid #ccc;
    }
    a {
      width: 100%;
      height: 35px;
      border-radius: 10%;
      line-height: 35px;
      margin-bottom: 10px;
      box-sizing: border-box;
      padding-left: 5px;
      font-weight: 400;
      font-size: 14px;
      display: inline-block;
      color: black;
      text-decoration: none;
      &:hover {
        // color: #1e80ff;
        background-color: rgb(247, 246, 246);
      }
    }
  }
}
</style>
