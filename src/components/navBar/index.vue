<template>
    <div class="navbar">
        <ul>
            <li><i class="icon icon-help">help</i></li>
            <li><i class="icon icon-search">search</i></li>
            <li><a href="javascript: void(0);" class="select-car-btn">选择车辆</a></li>
            <li><i class="icon icon-location">location</i></li>
            <li><i class="icon icon-user" @click="toUser">user</i></li>
            
        </ul>
    </div>
</template>

<script>
export default {
    name: "NavIndex",
    components:{},
    data(){
        return {
            
        }
    },
    methods:{
        toUser(){
            this.$router.push({
                name: "User"
            })
        }
    }
}
</script>

<style lang="scss">
/* 右侧导航栏 */
.navbar{
    position: fixed;
    left: 0;
    right: 0;
    bottom: 86px;
    z-index: 10;
    text-align: center;
    li{
        display: inline-block;
    }
    .icon{
        margin: 0 17px;
        //vertical-align 属性设置元素的垂直对齐方式。
        //middle: 把此元素放置在父元素的中部。
        vertical-align: middle;
        //文字颜色，后面要删了
        color: white;
        line-height: 44px;
        cursor: pointer;
    }
}

</style>