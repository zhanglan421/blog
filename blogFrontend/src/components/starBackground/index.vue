<template>
    <div class="star-wrap">
        <div class="star-content-1"></div>
        <div class="star-content-2"></div>
        <div class="star-content-3"></div>
        <div class="star-content-4"></div>
        <div class="star-content-5"></div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup() {


        return {}
    }
})
</script>

<style lang="scss" scoped>
.star-wrap {
    background: radial-gradient(#141720, #242a3d);
    width: 100vw;
    height: 100vh;

    @keyframes moveUp {
        0% {
            top: 0;
        }

        100% {
            top: -100vh;
        }
    }

    @function getMultiShadow($n) {
        $boxShadow: '#{random(100)}px #{random(100)}px #fff';

        @for $i from 1 through $n {
            $boxShadow: '#{$boxShadow} , #{random(100)}vw #{random(100)}vh #fff'
        }

        @return unquote($boxShadow);
    }

    @for $i from 1 through 5 {
        $size: unquote(floor(calc(5/$i)) + 'px');

        $count: random(120);

        $duration: unquote(random(20) + 's');

        .star-content-#{$i} {
            position: fixed;
            top: 0;
            left: 0;
            width: $size;
            height: $size;
            border-radius: 50%;
            background-color: #fff;
            box-shadow: getMultiShadow($count);
            animation: moveUp $duration linear infinite;

            &::after {
                content: '';
                position: absolute;
                top: 100vh;
                left: inherit;
                width: $size;
                height: $size;
                border-radius: 50%;
                background-color: #fff;
                box-shadow: inherit;
            }
        }
    }
}
</style>