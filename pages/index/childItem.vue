<template>
<div style="border-bottom: 1px solid red">
    <input v-model="item.name" style="border: 1px solid #333"/>
    改变这个值，父组件不会跟着改变
</div>
</template>

<script>
export default {
    name: "childItem",
    props: {
        item: Object,
    }
}
</script>

<style scoped>

</style>