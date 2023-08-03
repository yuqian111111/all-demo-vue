<template>
    <div class="wapper">
        <Headers></Headers>
        <Main>
        </Main>
        <Footervue></Footervue>
    </div>
</template>

<script>
import Headers from "./Header.vue"
import Main from "./main.vue"
import Footervue from "./Footer.vue"
export default {
    components: {
        Headers, Main, Footervue
    }
}
</script>

<style scoped>
.wapper {
    display: flex;
    flex-direction: column;
}

.wapper>>>.header {
    height: 48px;
    width: 100%;
    background-color: pink;
}

.wapper>>>.main {
    width: 100%;
    flex: 1;
    background-color: cyan;
    min-height: 400px;
    max-height: 400px;
    overflow-y: scroll;
}

.wapper>>>.footer {
    width: 100%;
    height: 120px;
    background-color: pink;
}
</style>