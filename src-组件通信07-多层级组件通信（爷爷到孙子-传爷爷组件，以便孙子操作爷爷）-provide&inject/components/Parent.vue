<template>
    <div>
        我是父组件
        <br>
        这里显示父级的msg:{{msg}}
        <Son></Son>
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
       /*
       传递组件本身不能使用对象模式，要使用函数模式
        provide:{
            test:"test provide inject",
            Parent:this,
        }, 
        */
       provide(){
           return {
            test:"test provide inject",
            Parent:this,
        };
       },
       data() {
           return {
               msg: "我是父级的msg"
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