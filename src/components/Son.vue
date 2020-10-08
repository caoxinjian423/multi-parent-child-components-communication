<template>
    <div>
        <hr>
        我是子组件
        <br>
        <button @click="handleMsg">点击改变msg</button>
        <Grandson v-bind="$attrs" v-on="$listeners"></Grandson>
       
    </div>
</template>

<script>
import Grandson from '../components/Grandson';
    export default {
        components: {
            Grandson,
        },
        inheritAttrs:false,
        created() {
            console.log("这里是子组件,改变之前的msg为:" + this.$attrs.msg);
        },
        updated () {
            console.log("这里是子组件,改变之后的msg为:" + this.$attrs.msg);
        },
        methods: {
            handleMsg() {
                this.$listeners.changeMsg("子组件更改的msg");
            }
        },
        
    }
</script>

<style scoped>

</style>