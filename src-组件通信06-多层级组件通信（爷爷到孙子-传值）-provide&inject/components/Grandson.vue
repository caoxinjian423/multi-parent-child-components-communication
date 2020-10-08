<template>
    <div>
        <hr>
        我是孙子组件
        <br>
        显示父组件provide中的test:{{test}}
    </div>
</template>

<script>
    export default {
        //孙子节点接收爷爷provide中定义的test
        inject:["test"],
    }
</script>

<style scoped>

</style>