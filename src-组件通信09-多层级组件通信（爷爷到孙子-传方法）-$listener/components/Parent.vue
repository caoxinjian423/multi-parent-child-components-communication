<template>
    <div>
        我是父组件
        <br>
        这里显示父级的msg:{{msg}}
        <Son :msg="msg" @changeMsg="changeMsg"></Son>
    </div>
</template>

<script>
/*
$listeners:
包含了父作用域中的 (不含 .native 修饰器的) v-on 事件监听器。它可以通过 v-on="$listeners" 
传入内部组件——在创建更高层次的组件时非常有用。
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