<template>
    <div>
        <!-- 右侧用户栏 -->
        <div id="children-view" :class="{open: show}">
            <router-view/>
        </div>
        <Map/>
        <Cars/>
        <Nav/>
    </div>
</template>

<script>
import Map from "../amap/index.vue"
import Cars from "../cars/index.vue"
import Nav from "../../components/navBar/index.vue"
export default {
    name: "Index",
    components:{ Map, Cars, Nav},
    data(){
        return {
        }
    },
    computed:{
        show(){
            const routerName = this.$route.name;
            return routerName === "Index" ? false : true;
        }
    },
    watch:{
        
    }
}
</script>

<style lang="scss">
#children-view{
    position: fixed;
    top: 0;
    bottom: 0;
    right: -600px;
    z-index: 101;
    width: 250px;
    background-color: #34393f;
    @include webkit(transition, all .3s ease 0s);//过渡
    &.open{
        right: 0;
    }
}
</style>