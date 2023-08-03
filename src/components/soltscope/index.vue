<template>
    <div>
        <slotChild :dataList="dataList">
            <template #item="ctx">
                <ul>
                    <li class="liitem" v-for="(item, i) in ctx.foo">
                        <span> 书名： {{ item.title }}</span>
                        <span>价格：{{ item.price }}</span>

                    </li>
                </ul>
            </template>
        </slotChild>
    </div>
</template>

<script>
import slotChild from "./slot-child.vue"
export default {
    components: { slotChild },
    data() {
        return {
            dataList: [
                {
                    title: "小王子与alice",
                    price: 1.0
                }, {
                    title: "灰姑娘",
                    price: 8.8
                }

            ]
        }
    }
}
</script>

<style scoped>
.liitem {
    background-color: pink;
    margin: 5px 0;
    list-style: none;
}
</style>