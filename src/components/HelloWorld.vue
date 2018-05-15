<template>
  <div class="hello">
    <h1>测试demo</h1>
    <div id='fuwenben'></div>
  </div>
</template>

<script>
var E = require('wangeditor');
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted(){
    var editor = new E('#fuwenben');
    editor.customConfig.menus = [
        'head',  // 标题
        'bold',  // 粗体
        'fontName',  // 字体
        'italic',  // 斜体
        'underline',  // 下划线
        'strikeThrough',  // 删除线
        'list',  // 列表
        'justify',  // 对齐方式
        'quote',  // 引用
        'image',  // 插入图片
    ]
    editor.customConfig.uploadImgShowBase64 = true
    editor.create()
    // editor.$textElem.attr('contenteditable', false)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .w-e-toolbar {
      display: -webkit-box;
      display: -ms-flexbox;
      display: flex;
      padding: 0 5px;
      flex-wrap: wrap;
  }
</style>
<style scoped>
h1, h2 {
  font-weight: normal;
      text-align: left;
    font-size: 0.6rem;
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
#fuwenben{
  width:7.5rem;
  overflow: hidden;
  height:400px;
  text-align:left;
}
</style>
