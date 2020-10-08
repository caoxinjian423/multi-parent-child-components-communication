<template>
    <div>
        <button :disabled="$attrs.disabled">点击</button>
    </div>
</template>

<script>
    export default {
          inheritAttrs: false,
    }
</script>

<style scoped>

</style>