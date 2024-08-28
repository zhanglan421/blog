<template>
    <div>
        你好
        <beian />
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import beian from '@/components/beian/index.vue'

export default defineComponent({
    components: {
        beian
    },
    setup () {
        

        return {}
    }
})
</script>

<style scoped>

</style>