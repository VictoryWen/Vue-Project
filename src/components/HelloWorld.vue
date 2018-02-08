<template>
  <div class="hello">
    <p>{{msg}}</p>
    <button @click="reverseMessage">逆转消息</button>

    <span :title="message">
      鼠标悬停几秒钟查看此处动态绑定的提示信息！
    </span>

    <p v-if="seen">你现在看见我了</p>

    <ol>
      <li v-for="todo in todos">
        {{ todo.text }}
      </li>
    </ol>

    <p>{{message}}}</p>

  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      message: '页面加载于' + new Date().toDateString(),
      seen: false,
      todos: [
        {text: '学习 JavaScript'},
        {text: '学习 Vue'},
        {text: '学习 efefv'}
      ]
    }
  },
  methods: {
    reverseMessage: function () {
      this.msg = this.msg.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
