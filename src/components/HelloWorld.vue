<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>HelloWorld!</h2>
    <lvshuy html="hello，lsy!" title="我是lvshuy组件内的值"/>
    <Child p1="今天天气好晴朗" v-on:cls='clk' />
    <send />
    <receive />
  </div>
</template>

<script>
import Child from './Child';
import send from './Send';
import receive from './Receive';
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    lvshuy: {
      props: ['html', 'title'],
      template: '<h3 v-bind:title="title">{{html}}</h3>'
      // template: '<h3 title=title>{{html}}</h3>'
    },
    Child,
    send,
    receive
  },
  methods: {
    clk:function(d){
      this.msg='Welcome lvshuy'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
  color: brown;
}
</style>
