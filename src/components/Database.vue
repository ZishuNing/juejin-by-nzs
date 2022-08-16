<template>
  <div></div>
</template>

<script>
export default {
  data() {
    return {
      database: [
        {
          id: 1,
          name: '稀土君',
          day: '15',
          category: 'java',
          title: '稀土开发者大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 2,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '开发者大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 3,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 4,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '开发者大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 5,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 6,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 7,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 8,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 9,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 10,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 11,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 12,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 13,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 14,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 15,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 16,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 17,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 18,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 19,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 20,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 21,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 22,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 23,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 24,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 25,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 26,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 27,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 28,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 29,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 30,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 31,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 32,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 33,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 34,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 35,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 36,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 37,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 38,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 39,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        },
        {
          id: 40,
          name: 'hhhh',
          day: '222',
          category: 'c++',
          title: '稀土大会出品人集结完毕，5折购票火热进行中！',
          intro: '来自各大互联网科技大厂的明星讲师正持续上线，5折购票火热进行中！',
          imgsrc: require('../assets/image/ArticleImg1.webp')
        }
      ]
    }
  },
  mounted() {
    this.$emit('emitData', this.database)
  }
}
</script>

<style></style>
