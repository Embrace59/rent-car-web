<template>
    <div class="cars-wrap">
        <section class="cars-item">
            <header>
                <h4 class="cars-logo">
                    <img src="../../assets/images/cars-logo.png" alt="Mustang 2019款">
                    <span class="cars-name">Mustang 2019款</span>
                </h4>
                <p class="cars-attr">新能源汽车 5座</p>
            </header>
            <div class="cars-content">
                <div class="cars-info">
                    <div>
                        <h4 class="cars-license">粤A88888</h4>
                        <div>
                            <ul class="cars-electirc">
                                <li></li>
                                <li></li>
                                <li></li>
                                <li></li>
                                <li></li>
                                <li></li>
                                <li></li>
                                <li></li>
                                <li></li>
                                <li></li>
                            </ul>
                            <p class="cars-distance">
                                <sub>约</sub>
                                <strong>600</strong>
                                <sub>KM</sub>
                            </p>
                        </div>
                    </div>
                </div>
                <img src="../../assets/images/pic001.jpg" alt="pic001">
            </div>
            <footer>
                <a href="javascript: void(0)" class="cars-parking">某某停车场</a>
            </footer>
        </section>
    </div>
</template>

<script>
import Map from "../amap/index.vue"
export default {
    name: "Cars",
    components:{ Map },
    data(){
        return {
        }
    },
    methods:{
        test(){
            this.$router.push({
                name: "User"
            });
        }
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
.cars-item{
    width: 505px;
    height: 240px;
    border-radius: 24px;
    margin: auto;//居中
    padding: 30px 30px 0;
    background-color: #fff;
    @include webkit(box-shadow, 0 0 18px 0 rgba(0, 0, 0, .2));
    @include webkit(box-sizing, border-box);
    header{
        display: flex;
        h4, p{
            flex: 1;
        }
    }
}

.cars-logo{
    img{
        display: inline-block;
        height: 34px;
        margin-right: 10px;
        vertical-align: middle;
    }
    .cars-name{
        line-height: 34px;
        font-size: 16px;
    }
}

.cars-attr{
    text-align: right;
    opacity: 5;
    line-height: 34px;
}

.cars-content{
    position: relative;
    margin: 11px, 0 7px;
    @extend %clearfix;
    //车辆信息
    .cars-info{
        display: flex;
        position: absolute;
        left: 0;
        right: 0;
        width: 100%;
        height: 100%;
        align-items: center;
        //车牌号
        .cars-license{
            font-size: 18px;
        }
        //电量
        .cars-electirc{
            display: inline-block;
            li{
                display: inline-block;
                width: 7px;
                height: 24px;
                margin-top: 10px;
                margin-right: 3px;
                background-color: #e1e1e1;
                border-radius: 100px;
            }
        }
        //距离
        .cars-distance{
            display: inline-block;
            strong{
                margin: 0 3px;
                font-size: 22px;
            }
            sub{
                position: relative;
                top: -1px;
            }
        }
    }
    //车辆图片
    img{
        float: right;
        height: 120px;
    }
}

.cars-parking{
    position: relative;
    display: block;
    border-top: 1px solid #e1e1e1;
    color: $color-main;
    opacity: .8;
    line-height: 53px;
    &:after{
        position: absolute;
        top: 23px;
        right: 0;
        content:"";
        width: 8px;
        height: 8px;
        border-top: 1px solid #d6d7d9;
        border-right: 1px solid #d6d7d9;
        @include webkit(transform, rotate(45deg));
    }
}

</style>