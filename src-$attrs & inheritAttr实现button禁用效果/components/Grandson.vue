<template>
    <div>
        <hr>
        我是孙子组件
        <br>
        {{$attrs.title}}
    </div>
</template>

<script>
    export default {
        inheritAttrs:false,
    }
</script>

<style scoped>

</style>