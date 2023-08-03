<template>
    <div>
        <slot name="item" :foo="dataList"></slot>
    </div>
</template>

<script>
export default {
    props: {
        dataList: {
            type: Array,
            default: []
        }
    },
}
</script>

<style scoped></style>