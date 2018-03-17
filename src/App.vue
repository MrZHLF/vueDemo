<template>
  <div id="app">
    <router-view></router-view>
    <HeaderTitle v-bind:title="title" v-on:titelChang='updateTitle($event)'></HeaderTitle>
    <MainText v-bind:users="users"></MainText>
    <MainText v-bind:users="users"></MainText>
    <FooterTitle v-bind:title="title"></FooterTitle>
  </div>
</template>

<script>
import HeaderTitle from './components/HeaderTitle'
import MainText from './components/MainText'
import FooterTitle from './components/FooterTitle'
export default {
  name: 'app',
  data () {
    return {
      users: [
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false},
        {name: '你的职位', position: 'web前端', show: false}
      ],
      title: '传递的是一个值(number string,boolean)'
    }
  },
  methods: {
    updateTitle (title) {
      this.title = title
    }
  },
  components: {
    HeaderTitle,
    MainText,
    FooterTitle
  }
}
</script>

<style>
</style>
