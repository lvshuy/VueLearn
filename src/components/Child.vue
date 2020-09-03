<template>
  <div>
      <p>{{p1}}</p>
      <input type="button" value="测试" @click="clkhander">
  </div>
</template>

<script>
export default {
    name: 'Child',
    props: {
        p1: {
            type: String,
            required: true
        }
    },
    methods: {
        clkhander:function(){
            this.$emit('cls', '23333')
        }
    }
}
</script>
