<template>
    <div>
        <hr>
        我是子组件
        <br>
         {{$attrs.title}}
        <Grandson v-bind="$attrs"></Grandson>
       
    </div>
</template>

<script>
import Grandson from '../components/Grandson';
    export default {
        components: {
            Grandson,
        },
        inheritAttrs:false,
        mounted () {
            console.log(this.$attrs);
        },
        
    }
</script>

<style scoped>

</style>