<template>
    <!--子组件,定义事件函数，函数中为该组件,在绑定一个事件，然后父组件，在定义的这个时间中，调用自己的方法-->
    <li @click = 'handleDelete'>{{content}}</li>
</template>

<script>
export default {
  name: 'todoItem',
  props: [ 'content', 'index' ],
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    handleDelete: function () {
      this.$emit('delete', this.index)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.li{
  background-color: chartreuse;
  color: rebeccapurple;
}
</style>
