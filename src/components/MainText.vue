<template>
    <div class="main">
        <ul>
            <li v-for="user in users" v-on:click="user.show = !user.show">
                <h2>{{user.name}}</h2>
                <h3 v-show="user.show">{{user.position}}</h3>
            </li>
        </ul>
        <button v-on:click="delterUser">删除</button>
    </div>
</template>

<script>
export default {
  name: 'MainText',
  // props: ['users'],  父组件向子组件传递数据
  props: {
    users: {
      type: Array,
      required: true
    }
  },
  data () {
    return {
    }
  },
  methods: {
    delterUser: function () {
      this.users.pop()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">
.main{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
    ul{
        display: flex;
        flex-wrap: wrap;
        list-style: none;
        padding: 0;
        li {
            flex-grow: 1;
            flex-basis: 300px;
            text-align: center;
            border: 1px solid #222;
            margin: 20px;
            height: 100px;
            h2{
                font-weight: 500;
                line-height: 50px;
            }
            &:hover{
                background: rgba(0,0,0,0.5);
                color: #fff;
            }
        }
    }
}
</style>
