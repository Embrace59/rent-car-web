<template>
    <div>
        <!-- 车辆卡片 -->
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


        <section class="cars-item cars-detail" :style="'height:' + height">
            <h4 class="column">
                某某停车场
                <i class="close"></i>
            </h4>
            <header>
                <h4 class="cars-logo">
                    <img src="../../assets/images/cars-logo.png" alt="Mustang 2019款">
                    <span class="cars-name">Mustang 2019款</span>
                </h4>
                <p class="cars-attr">新能源汽车 5座</p>
            </header>
            <img src="../../assets/images/pic001.jpg" alt="pic001" class="bigCarImg">
            <div class="clearfix">
                <h4 class="cars-license pull-left">粤A88888</h4>
                <p class="cars-distance pull-right">
                    <sub>约</sub>
                    <strong>600</strong>
                    <sub>KM</sub>
                </p>
            </div>
            <div class="cars-electirc-strip">
                <span class="e-bg"></span>
                <div class="e-high"></div>
            </div>
            <p class="cost-info">取车约支付12.0元停车费，实际补贴12.0元</p>
            <ul class="cars-type-list">
                <li class="current">
                    <p class="name">日租车</p>
                    <span class="price">￥120元/时</span>
                </li>
                <li>
                    <p class="name">日租车</p>
                    <span class="price">￥120元/时</span>
                </li>
                <li>
                    <p class="name">日租车</p>
                    <span class="price">￥120元/时</span>
                </li>
                <li>
                    <p class="name">日租车</p>
                    <span class="price">￥120元/时</span>
                </li>
            </ul>
            <div class="detail-footer clearfix">
                <span class="detail-footer-insurance">用车保障</span>
                <i class="current"></i>
                <i></i>
            </div>
            <li><a href="javascript: void(0);" class="select-car-btn">预约车辆</a></li>
        </section> 
    </div>
</template>

<script>
export default {
    name: "CarsItem",
    components:{ },
    props: {
        height:{
            type: String,
            default: "220px"
        }
    },
    data(){
        return {
        }
    },
    methods:{
    }
}
</script>

<style lang="scss">

.cars-item{
    width: 440px;
    height: 220px;
    border-radius: 24px;
    margin: auto;//居中
    padding: 20px 20px 0;
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
        height: 28px;
        margin-right: 10px;
        vertical-align: middle;
    }
    .cars-name{
        line-height: 34px;
        font-size: 14px;
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
        
    }
    //车辆图片
    img{
        float: right;
        height: 110px;
    }
}

//车牌号
.cars-license{
    font-size: 16px;
}
//距离
.cars-distance{
    display: inline-block;
    strong{
        margin: 0 3px;
        font-size: 20px;
    }
    sub{
        position: relative;
        top: -1px;
    }
}
//小卡片停车场
.cars-parking{
    position: relative;
    display: block;
    border-top: 1px solid #e1e1e1;
    color: $color-main;
    opacity: .8;
    line-height: 53px;
    font-size: 14px;
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

.cars-detail{
    //display: none;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    .column{
        position: relative;
        padding: 0 0 8px;
        margin-bottom: 2px;
        font-size: 14px;
        color: #34393f;
        border-bottom: 1px solid #e1e1e1;
        .close{
            position: absolute;
            display: block;
            width: 16px;
            height: 16px;
            right: 0;
            top: 2px;
            cursor: pointer;
            &:before, &:after{
                content: "";
                position: absolute;
                top: 50%;
                left: 50%;
                margin-left: -1px;
                margin-top: -10px;
                height: 20px;
                border-left: 2px solid #999c9f;
            }
            &:before{
                @include webkit(transform, rotate(45deg));
            }
            &:after{
                @include webkit(transform, rotate(-45deg));
            }
        }
    }
    .select-car-btn{
        position: absolute;
        bottom: -32px;
        left: 100px;
    }
}

.bigCarImg{
    width: 300px;
    margin: 0 45px;
}

.cars-electirc-strip{
    width: 400px;
    height: 24px;
    margin-top: 8px;
    position: relative;
    border-radius: 100px;
    background-color: #fff;
    @include webkit(box-shadow, 0 0 10px 0 rgba(0, 0, 0, .1));
    .e-bg{
        display: block;
        width: 380px;
        height: 8px;
         //居中
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        margin: auto;
        border-radius: 100px;
        background-color: #e1e1e1;

    }
    .e-high{
        width: 180px;
        height: 8px;
        //居中
        position: absolute;
        left: 10px;
        top: 8px;
        margin: auto;
        z-index: inherit + 1;
        border-radius: 100px;
        background-color: #0f9cee;
    }
}

.cost-info{
    font-size: 12px;
    color: $color-main;
    text-align: center;
    margin: 12px 0;
}

.cars-type-list{
    li{
        height: 43px;
        margin: 10px 0;
        padding: 0 17px 0 20px;
        background-color: #f3f3f3;
        border-color: #f3f3f3;
        border-style: solid;
        border-width: 2px;
        border-radius: 10px;
        line-height: 43px;
        font-size: 16px;
        cursor: pointer;
        &.current{
            border-color: #0f9cee;
        }
    }
    .name{
        float: left;
    }
    .price{
        float: right;
    }
}

.detail-footer{
    position: relative;
    .detail-footer-insurance{
        float: left;
    }
    i{
        float: right;
        display: block;
        width: 15px;
        height: 15px;
        margin: 5px 5px;
        background-color: pink;
        border-radius: 100px;
        &.current{
            background-color: black;
        }
        &:before{
            position: absolute;
            content: "";
            width: 10px;
            height: 7px;
            // margin: 0 0 0 5px ;
            margin-left: 2px;
            margin-top: 1px;
            border-left: 2px solid #fff;
            border-bottom: 2px solid  #fff;
            @include webkit(transform, rotate(-45deg));
        }
    }
}

</style>