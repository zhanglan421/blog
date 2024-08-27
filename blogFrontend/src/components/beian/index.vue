<template>
    <div class="beian-content" @click="onClickBeian">
        蜀ICP备2023030024号-1
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup () {
        const onClickBeian = () => {
            window.open('https://beian.miit.gov.cn/')
        }

        return {
            onClickBeian
        }
    }
})
</script>

<style scoped>
    .beian-content {
        position: fixed;
        bottom: 1vh;
        left: 50%;
        transform: translateX(-50%);
        color: #fff;
        cursor: pointer;
        font-size: 12px;
        opacity: 0.4;
    }
</style>