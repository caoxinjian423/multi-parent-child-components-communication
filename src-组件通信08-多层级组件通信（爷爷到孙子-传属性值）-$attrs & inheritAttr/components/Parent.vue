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
$attrs:
包含了父作用域中不作为 prop 被识别 (且获取) 的 attribute 绑定 (class 和 style 除外)。
当一个组件没有声明任何 prop 时，这里会包含所有父作用域的绑定 (class 和 style 除外)，并且
可以通过 v-bind="$attrs" 传入内部组件。

inheritAttrs:
默认为true,默认情况下父作用域的不被认作 props 的 attribute 绑定 (attribute bindings) 
将会“回退”且作为普通的 HTML attribute 应用在子组件的根元素上。当撰写包裹一个目标元素或
另一个组件的组件时，这可能不会总是符合预期行为。通过设置 inheritAttrs 到 false，
这些默认行为将会被去掉。而通过 (同样是 2.4 新增的) 实例 property $attrs 可以让这些
 attribute 生效，且可以通过 v-bind 显性的绑定到非根元素上。
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