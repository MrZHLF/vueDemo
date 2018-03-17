<template>
    <header v-on:click="ChangClick">
        <h1>{{msg}}{{title}}</h1>
    </header>
</template>

<script>
export default {
  name: 'HeaderTitle',
  props: {
    title: {
      type: String
    }
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    ChangClick () {
      // this.title = '我改变了'
      this.$emit('titelChang', '子向父组件传值')
    }
  },
  beforeCreate: function () {
    alert('组件创建前')
  },
  created: function () {
    alert('组件实列化完，但页面还未显示')
  },
  beforeMount: function () {
    alert('组件挂载前，页面任未展示，但虚拟DOM已经配置')
  },
  mounted: function () {
    alert('组件挂载后，此方法执行后，页面显示')
  },
  beforeUpdate: function () {
    alert('组件更新前，页面任未更新，但虚拟DOM已经配置好了')
  },
  updated: function () {
    alert('组件更新后，此方法执行，页面显示出来')
  },
  beforeDestory: function () {
    alert('组件销毁前')
  },
  destoryed: function () {
    alert('组件销毁后')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">
*{
    margin: 0;
    padding: 0;
}
header {
    width: 100%;
    height: 50px;
    background: #222;
    h1{
        color: #fff;
        text-align: center;
        line-height: 50px;
    }
}
</style>
