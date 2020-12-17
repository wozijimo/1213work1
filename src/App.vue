<template>

<!-- 只允许有一个直接子元素 -->
  <div id="app">
    {{message}}

    <!-- v-bind指令 -->
    <span v-bind:title="message">我是span标签</span>

    <!-- v-for指令 -->
    <div v-for="(item,index) in arr" :key="index">{{item}}</div>

    <!-- v-if指令 -->
    <div v-if="false">我是if指令</div>
    <div v-else-if="true">我是if指令 else if 分支</div>
    <div v-else>我是if指令 else 分支</div>
    

    <!-- v-on指令 -->
    <div v-on:click="test"></div>

    <!-- v-model指令 -->
    <input type="text" v-model="val"/>
    <div>我是输入框的值:{{val}}</div>

    <!-- 计算器 -->
    <div class="cls-counter">
      <input type="number" v-model.number="number1">
      <select v-model="opt">
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">/</option>
      </select>
      <input type="number" v-model.number="number2">
      <div>=</div>
      <button v-on:click="conput()">计算</button>
      <div>{{sum}}</div>
    </div>
    <div v-if="opt == `+`">我是运算结果{{number1+number2}}</div>
    <div v-if="opt == `-`">我是运算结果{{number1-number2}}</div>
    <div v-if="opt == `*`">我是运算结果{{number1*number2}}</div>
    <div v-if="opt == `/`">我是运算结果{{number1/number2}}</div>
    <div>我是运算符:{{opt}}</div>


    <!-- 百度新闻 -->
    <div class="newsItem" v-for="item in baidunews" :key="item.i">
      <div v-bind:class="[item.i == 1?`cls1`:item.i == 2 ?`cls2`:item.i == 3 ? `cls3`:`cls`]">{{item.i}}</div>
      <div>{{item.title}}</div>
      <div>{{item.con}}</div>

    </div>








  </div>
</template>

<script>

export default {

  name: 'App',
  data(){
    return{
      message:"hello",
      arr:[10,20,30,40],
      val:"我是val",
      opt:"+",
      number1:0,
      number2:0,
      sum:0,
      baidunews:[{
        i:1,
        title:"我是标题1",
        con:"100W"
      },{
        i:2,
        title:"我是标题2",
        con:"200W"
      },{
        i:3,
        title:"我是标题3",
        con:"300W"
      },{
        i:4,
        title:"我是标题4",
        con:"400W"
      }],
    };
  },

    methods: {
    test(){
      console.log("被点击了");
    },
    conput(){
      switch(this.opt){
        case "+":
          this.sum = this.number1+this.number2;
        break;
        case "-":
          this.sum = this.number1-this.number2;
        break;
        case "*":
          this.sum = this.number1*this.number2;
        break;
        case "/":
          this.sum = this.number1/this.number2;
        break;

      }
    }
  }
}




</script>

<style> 
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.cls-counter{
  display: flex;
  flex-flow: row;
  justify-content: center;
}

/* 百度新闻item */
.newsItem{
  width: 400px;
  height: auto;
  display: flex;
  flex-flow: row;
  justify-content: space-around;
  align-items: center;
  background-color: #cccccc;
}

.cls{
  color: #999999;
}

.cls1{
  color: #A52A2A;
}

.cls2{
  color: #FFA54F;
}

.cls3{
  color: #FF1493;
}


</style>
