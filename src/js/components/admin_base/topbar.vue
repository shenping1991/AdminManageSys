<template>
    <div class="topbar">
        <!--  -->
        <div class="headerWrapper">
            <header class="header">
                <div class="container">
                <h1 class="fl ">
                    <a href="#" class="router-link-active">
                    后台管理系统
                    </a>
                </h1>
                <el-button class="fr mr30 mt15"  type="warning" plain size="small" @click="loginOut">log out</el-button>
                <el-menu :default-active="activeIndex2" class="fr el-menu-demo" mode="horizontal" @select="handleSelect" background-color="rgba(70, 76, 91, 1)" text-color="#ffffff" active-text-color="#ffd04b">
                    <el-menu-item index="1">处理中心</el-menu-item>
                    <el-submenu index="2">
                    <template slot="title">我的工作台</template>
                    <el-menu-item index="2-1">选项1</el-menu-item>
                    <el-menu-item index="2-2">选项2</el-menu-item>
                    <el-menu-item index="2-3">选项3</el-menu-item>
                    <!-- <el-submenu index="2-4">
                        <template slot="title">选项4</template>
                        <el-menu-item index="2-4-1">选项1</el-menu-item>
                        <el-menu-item index="2-4-2">选项2</el-menu-item>
                        <el-menu-item index="2-4-3">选项3</el-menu-item>
                    </el-submenu> -->
                    </el-submenu>
                    <el-menu-item index="3" disabled>消息中心</el-menu-item>
                </el-menu>
                
                </div>
            </header>
        </div>
    </div>
</template>

<script>
    export default {
    data() {
      return {
        activeIndex2: '1',
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      },
      loginOut(){

      }
    }
  }
</script>
<style lang="scss" >
    .topbar {
        background: rgba(255,160,0,1);
        width: 100%;
        height: 60px;
        box-shadow: 3px 0 10px rgba(0, 0, 0, .1);
    }
    .container{
        padding: 0 20px;
    }
    .header h1{
        margin: 0;
        float: left;
        font-size: 32px;
        font-weight: 400;

    }
    .header h1 a{
        color: #fff;
        font-size: 22px;
    }
    .el-menu{
        background: #ffa000;
    }
    .el-menu--horizontal {
        .el-menu-item {
            color: #fff;
            background: #ffa000 !important;
            &.is-active {
                background: #ffa000;
                color: #fff;
                border-bottom: 3px solid rgba(255,255,255,0.8);
            }
            &:hover {
                background: #ffa000;
                color: #fff;
                border-bottom: 3px solid rgba(255,255,255,0.3) !important;
            }
        }

        .el-submenu {
            // &.is-active,&:hover{
            //         background: #ffa000;
            //         color: #fff;
            &:hover{
                .el-submenu__title{
                    border-bottom: 3px solid rgba(255,255,255,0.3) !important;
                }
            }
                border-bottom: 0;
                .el-menu-item{
                    border-bottom: 3px solid rgba(255,255,255,0.3);
                }
                .el-submenu__title{
                    background-color: #ffa000;
                    color: #fff;
                    height: 57px;
                    line-height: 57px;
                    border-bottom: 0;
                    .is-active {
                        background: #ffa000;
                        color: #fff;
                        border-bottom: 0;
                    }
                    &:hover{
                        background: #ffa000;
                        color: #fff;
                        border-bottom: 0;
                    }
                }
                .el-submenu__icon-arrow {
                    position: static;
                    vertical-align: middle;
                    margin-left: 5px;
                    color: #ffffff !important;
                    margin-top: -3px;
                }
                .el-menu-item {
                    background: #fff !important;
                    color:#585858;
                    border: 0 !important;
                    &:hover {
                        background: #f1f1f1 !important;
                    }
                }
            // }        
        }
        
    }
    .header .el-button{
        margin-top: 15px !important;
        border: 0 !important;
        color:#ffa000 !important;
    }
</style>
