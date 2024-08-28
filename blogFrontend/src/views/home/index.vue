<template>
    <div>
        <div class="home-content">你好，我有一个帽衫，我要在网上问问</div>

        <vue-particles id="tsparticles" :options="tsparticlesConfig" />

        <starBackground />

        <beian />
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import beian from '@/components/beian/index.vue'
import starBackground from '@/components/starBackground/index.vue'

import { tsparticlesConfig } from '@/config/tsparticles.config'

export default defineComponent({
    components: {
        beian,
        starBackground
    },
    setup() {


        return {
            tsparticlesConfig
        }
    }
})
</script>

<style lang="scss" scoped>
.home-content {
    position: relative;
    display: flex;
    width: 100%;
    height: 100vh;
    justify-content: center;
    align-items: center;
    color: #fff;
    font-size: 30px;
    z-index: 999;
    
    &::selection {
        background-color: transparent;
    }
}
</style>