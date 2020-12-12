<template>
    <div class="user-container">
        <Back column="安全设置"/>
        <ul class="group-links">
            <router-link to="/password" tag="a" class="arrow">
                <span>修改登录密码</span>
            </router-link>
             <router-link to="aa" tag="a" class="arrow">
                <span>设置资金密码</span>
            </router-link>
             <router-link to="aa" tag="a" class="arrow">
                <span>绑定手机号</span>
            </router-link>
             <router-link to="aa" tag="a" class="arrow">
                <span>绑定银行号</span>
            </router-link>
        </ul>
    </div>
</template>

<script>
export default {
    name: "safeIndex",
    components:{},
    data(){
        return {
        }
    },
}
</script>

<style lang="scss">


</style>