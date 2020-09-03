// 通过按钮发送
<template>
  <div>
      <input type="button" value="send" @click="clkhander">
  </div>
</template>

<script>
import pub from './pub'
export default {
    name: 'send',
    methods: {
        clkhander:function(){
            pub.$emit("clk2", 'send message')
        }
    }
}
</script>

<style>

</style>