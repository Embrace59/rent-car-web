<template>
    <div class="user-container">
        <div class="user-info">
            <img src="../../assets/images/logo.png" alt="logo">
            <div class="meta">
                <h4 class="user-name">ljdx678@163.com</h4>
                <span>
                    文明驾驶分
                    <strong>60</strong>
                </span>
            </div>
        </div>
        <ul class="group-links">
            <router-link to="aa" tag="a" class="arrow">
                <i class="icon icon-user-link-1"></i>
                <span>我的帐户</span>
            </router-link>
             <router-link to="aa" tag="a" class="arrow">
                <i class="icon icon-user-link-2"></i>
                <span>租车订单</span>
            </router-link>
             <router-link to="aa" tag="a" class="arrow">
                <i class="icon icon-user-link-3"></i>
                <span>实名认证</span>
            </router-link>
             <router-link to="/safe" tag="a" class="arrow">
                <i class="icon icon-user-link-4"></i>
                <span>安全设置</span>
            </router-link>
             <router-link to="aa" tag="a" class="arrow">
                <i class="icon icon-user-link-5"></i>
                <span>帮助中心</span>
            </router-link>
        </ul>
         <button class="logout">登出</button>
    </div>
</template>

<script>
export default {
    name: "user",
    components:{  },
    data(){
        return {
        }
    },
}
</script>

<style lang="scss">
.user-container{
    padding: 0 20px;
    .user-info{
        padding: 60px 0 0 10px;
        display: flex;
        img{
            width: 80px;
            height: 80px;
        }
        .meta{
            flex: 1;
            padding-left: 20px;
        }
        .user-name{
            color: #909090;
            line-height: 43px;
            font-size: 18px;
        }
        span{
            display: inline-block;
            height: 27px;
            padding: 0 17px;
            background-color: #10a0f2;
            line-height: 27px;
            border-radius: 100px;
            color: #fff;
            font-size: 13px;
        }
    }
}

.logout {
    position: absolute;
    left: 50%;
    bottom: 60px;
    width: 165px;
    height: 58px;
    margin-left: -82px;
    background-color: #2d3339;
    border-radius: 100px;
    text-align: center;
    line-height: 58px;
    color: #fff;
    font-size: 18px;
    border: none;
    outline: none;
    
}
</style>