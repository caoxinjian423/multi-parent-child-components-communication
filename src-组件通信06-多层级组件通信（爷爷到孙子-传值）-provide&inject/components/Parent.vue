<template>
    <div>
        我是父组件
        <Son></Son>
    </div>
</template>

<script>
/*
provide：Object | () => Object
inject：Array<string> | { [key: string]: string | Symbol | Object }

这对选项需要一起使用，以允许一个祖先组件向其所有子孙后代注入一个依赖，不论组件层次有多深，并在其上下游关系成立的时间里
始终生效。如果你熟悉 React，这与 React 的上下文特性很相似。

provide 选项应该是一个对象或返回一个对象的函数。该对象包含可注入其子孙的 property。在该对象中你可以使用 
ES2015 Symbols 作为 key，但是只在原生支持 Symbol 和 Reflect.ownKeys 的环境下可工作。

inject 选项应该是：
一个字符串数组，或一个对象，对象的 key 是本地的绑定名，value 是：在可用的注入内容中搜索用的 key (字符串或 Symbol)，
或一个对象，该对象的：from property 是在可用的注入内容中搜索用的 key (字符串或 Symbol)
default property 是降级情况下使用的 value
 */
 import Son from '../components/Son';
    export default {
       components: {
           Son,
       },
        provide:{
            test:"test provide inject"
        }, 
    }
</script>

<style scoped>

</style>