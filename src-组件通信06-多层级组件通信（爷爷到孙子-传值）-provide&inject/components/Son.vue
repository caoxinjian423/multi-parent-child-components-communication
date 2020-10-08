<template>
    <div>
        <hr>
        我是子组件
        <Grandson></Grandson>
    </div>
</template>

<script>
import Grandson from '../components/Grandson';
    export default {
        components: {
            Grandson,
        },
        
    }
</script>

<style scoped>

</style>