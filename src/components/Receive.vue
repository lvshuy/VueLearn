// 接收
<template>
  <div>
      <p>{{tip}}</p>
  </div>
</template>

<script>
import pub from './pub'
export default {
    name: 'receive',
    data () {
        return {
            tip: '发送前'
        }
    },
    mounted: {
        clkhander:function(){
            pub.$on("clk2",(data)=>{
                this.tip=data;
            })
        }
    }
}
</script>

<style>

</style>