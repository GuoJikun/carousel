<template>
    <div class="fox-carousel">
        <div class="fox-carousel__page">
            <slot name="page"></slot>
        </div>
        <div class="fox-carousel__wrap">
            <slot></slot>
        </div>
        <div class="fox-carousel__indicator">
            <slot name="indicator">
                <ol class="fox-carousel__indicator-container">
                    <template v-for="i in count">
                        <li class="fox-carousel__indicator-item" :key="i">{{ i }}</li>
                    </template>
                </ol>
            </slot>
        </div>
    </div>
</template>
<script>
import { prefix } from "@/utils/const.js";
export default {
    name: `${prefix}Carousel`,
    props: {
        height: String,
    },
    provide() {
        return {
            height: this.height,
        };
    },
    data() {
        return { count: 0, children: [] };
    },
    mounted() {
        this.count = this.$slots.default.length;
    },
};
</script>

<style lang="scss">
.fox-carousel {
    display: block;
    &__indicator {
        position: relative;
    }
}
</style>
