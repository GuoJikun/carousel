<template>
    <div>
        <slot></slot>
    </div>
</template>
<script>
import { prefix } from "@/utils/const.js";
export default {
    name: `${prefix}CarouselItem`,
};
</script>
