<template>
    <div>
        <hr>
        我是孙子组件
        <br>
        <button @click="handleMsg">点击改变msg</button>
        {{$attrs.title}}
    </div>
</template>

<script>
    export default {
        inheritAttrs:false,
        beforeUpdate () {
            console.log("这里是孙子组件,改变之前的msg为:" + this.$attrs.msg);
        },
        updated () {
            console.log("这里是孙子组件,改变之后的msg为:" + this.$attrs.msg);
        },
        methods: {
           handleMsg() {
                this.$listeners.changeMsg("孙子组件更改的msg");
            }
        },
    }
</script>

<style scoped>

</style>