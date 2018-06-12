<template>
<div>
    <div class="app">
        {{message}}
    </div>
    <div class="app-bind">
        <span v-bind:title="message1"> 鼠标悬停几秒钟查看此处动态绑定的提示信息！ </span>
    </div>
    <div class="app-for">
        <ol>
            <li v-for="todo in todos">
                {{todo}}
            </li>
        </ol>
    </div>
    <div class="app-on">
        <p>{{reverseMsg}}</p>
        <button v-on:click="reverseMessage"> {{reverseMsg}}</button>
    </div>
    <div class="app-model">
        <p>{{messageModel}}</p>
<input type="text" v-model="messageModel">
    </div>
</div>
    
    
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      message: "hello world!",
      message1: "页面加载于 " + new Date().toLocaleString(),
      todos: [
        { text: "学习 JavaScript" },
        { text: "学习 Vue" },
        { text: "整个牛项目" }
      ],
      reverseMsg: "逆转消息",
      messageModel: "你好！🍎"
    };
  },
  created() {
    setInterval(() => {
      this.message = "hello world!" + new Date().toLocaleString();
    });
  },
  methods: {
    reverseMessage() {
      this.reverseMsg = this.reverseMsg
        .split("")
        .reverse()
        .join("");
    }
  }
};
</script>

<style>
</style>





