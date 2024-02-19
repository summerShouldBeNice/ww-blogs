<template>
  <div class="entry-content">
    <div v-highlight v-html="article" id="content"></div>
  </div>
</template>

<script>
// 将marked 引入
import {marked} from 'marked';

export default {
  name: 'App',
  data() {
    return {
      article: ''
    }
  },
  mounted() {
    // this.article = "<h1> 1111 </h1> <div> 222</div>"
    this.article = marked('## Mac 创建vue项目报错\n' +
        '\n' +
        'Vue3 在创建项目的时候会失败， 尝试使用管理员权限创建在vue create命令前加上 sudo\n' +
        '\n' +
        '创建成功后使用 npm run serve失败， 尝试给目标文件权限 sudo chmod -R 777 target-file\n' +
        '\n')
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
