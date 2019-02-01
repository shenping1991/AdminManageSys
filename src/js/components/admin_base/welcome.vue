<template>
    <div class="welcome-wrap">
    <p>welcomevue</p>
        <img src="" alt="">
    </div>
</template>
<script>
    export default{
        data(){
            return{
                name:'welcome'
            }
        }
    }
</script>
<style lang="scss" scoped>
    .welcome-wrap{
        height: 100%;
        width: 100%;
        img{
            display: block;
            width: 100%;
            height: 100%;
        }
        .hd{
            font-size: 30px;
            text-align: center;
        }
        .bd{

        }
    }
</style>
<style lang="scss">
    .welcome-steps{
        .el-step__line-inner{
            height: 100% !important;
        }
    }
</style>
