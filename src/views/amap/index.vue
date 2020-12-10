<template>
    <div class="amap-wrap">
        <el-amap
            vid="amapDemo"   
            class="amap-demo"
            :events="events">
        </el-amap>
    </div>
</template>

<script>
import { AMapManager, lazyAMapApiLoaderInstance } from 'vue-amap';
export default {
    name: "Amap",
    data(){
        return {
            map: null,
            //地图缩放的范围，在PC上，默认范围[3,18]，取值范围[3-18]
            zoom: 18,
            events: {}
        }
    },

    mounted(){
        lazyAMapApiLoaderInstance.load().then(() => {
            // your code ...
            this.map = new AMap.Map('amapContainer', {
                center: new AMap.LngLat(121.59996, 31.197646),
                zoom: this.zoom
            });
        });
    }
}
</script>

<style lang="scss">
.amap-wrap{
    height: 100vh;
}
</style>