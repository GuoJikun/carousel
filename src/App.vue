<template>
    <div id="app">
        <h1>Carousel 轮播图</h1>

        <div>
            <h2>基础用法</h2>
            <div>
                <fox-carousel height="300">
                    <fox-carousel-item></fox-carousel-item>
                    <fox-carousel-item></fox-carousel-item>
                    <fox-carousel-item></fox-carousel-item>
                </fox-carousel>
            </div>
        </div>
    </div>
</template>

<script>
import FoxCarousel from "./components/carousel";
import FoxCarouselItem from "./components/carousel-item";

export default {
    name: "App",
    components: {
        FoxCarousel,
        FoxCarouselItem,
    },
    data() {
        return {
            list: [1, 2, 3, 4],
        };
    },
};
</script>

<style lang="scss">
#app {
    width: 1100px;
    margin: 0 auto;
    font-size: 14px;
    box-sizing: border-box;
    font-family: Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, SimSun, sans-serif;
    font-weight: 400;
}
body {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
h1,
h2 {
    font-weight: 600;
}
h1 {
    font-size: 18px;
}
h2 {
    font-size: 16px;
}
</style>
