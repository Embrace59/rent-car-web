<template>
    <div class="cars-wrap">
        <div class="cars-swiper-wrap">
            <swiper class="swiper" :options="swiperOption">
                <swiper-slide><CarsItem /></swiper-slide>
                <swiper-slide><CarsItem height="600px"/></swiper-slide>
                <swiper-slide><CarsItem/></swiper-slide>
                <swiper-slide><CarsItem/></swiper-slide>
                <swiper-slide><CarsItem/></swiper-slide>
                <div class="swiper-button-prev" slot="button-prev"></div>
            <div class="swiper-button-next" slot="button-next"></div>
            </swiper>
        </div>
    </div>
</template>

<script>
import Map from "../amap/index.vue"
import CarsItem from "../../components/carsList/index.vue"
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/swiper-bundle.css'
export default {
    name: "Cars",
    components:{ 
        Map, 
        Swiper, 
        SwiperSlide, 
        CarsItem
    },
    data(){
        return {
            swiperOption: {
                slidesPerView: 3,
                spaceBetween: 30,
                navigation: {
                    nextEl: '.swiper-button-next',
                    prevEl: '.swiper-button-prev'
                }
            },
            
        }
    },
    methods:{
    }
}
</script>

<style lang="scss">

.cars-wrap{
    position: fixed;
    left: 0;
    bottom: 94px;
    right: 0;
    z-index: 11;
}

.cars-swiper-wrap{
    .swiper-container{
        overflow: initial;
    }
    .swiper-button-prev, .swiper-button-next{
        width: 50px;
        height: 80px;
        border-radius: 100px;
        background-color: #fff;
        @include webkit(box-shadow, 0 0 18px 0 rgba(0, 0, 0, .2));
        @include webkit(transition, all .3s ease 0s);//过渡
        &:hover{
            background-color: $color-main;
        }
    }
}
</style>