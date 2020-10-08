<template>
    <div>
        我是父组件
        <br>
        这里显示父级的msg:{{msg}}
        <Son :title="title"></Son>
    </div>
</template>

<script>
/*
provide 、inject只能父级给子孙后代传递参数，而不知道子孙后代到底有多少，子孙后代怎么操作父级呢？
解决这个问题就需要父级把自己也传递给子孙后代
 */
 import Son from '../components/Son';
    export default {
       components: {
           Son,
       },
       data() {
           return {
               msg: "我是父级的msg",
               title:"我是父级传递的title"
           };
       },
       methods: {
           changeMsg(msg) {
               this.msg = msg;
           },
       },
    }
</script>

<style scoped>

</style>